---
layout: guia
title: Automação com Tasker | PressVibe
description: Como acionar botões do PressVibe pelo Tasker e outros apps de automação.
permalink: /apps/pressvibe/automacao/
---

# Automação com Tasker

A automação deixa outros apps do mesmo celular, como o Tasker, acionarem o PressVibe. O outro app nunca vê as chaves dos seus serviços. Ele só conhece um código de integração, que você troca quando quiser.

Casos de uso: disparar um alerta quando o celular detecta uma queda, avisar que você chegou ao chegar em casa, ou encerrar o Ping quando você conecta no Wi-Fi de casa.

## Ligar a integração

1. Abra **Configurações > Automação (Tasker)**.
2. Ligue **Permitir automação**. O app gera o **Código de integração**.
3. Marque os **Botões que outros apps podem acionar**.
4. Marque os **Destinos pelos quais outros apps podem enviar**, se for usar a ação Enviar mensagem.

A automação vem desligada, e cada botão e destino precisa ser liberado um a um. Um pedido com código errado é recusado e registrado no histórico, sem guardar o conteúdo do pedido.

Se o código vazar, toque em **Novo código**. O antigo para de funcionar na hora, então copie o novo para o Tasker.

## Configurar no Tasker

O próprio app tem a tela **Como configurar o Tasker**, que monta os valores com os nomes dos seus botões e tem botão de copiar em cada campo. Prefira usá-la. O resumo abaixo serve de referência.

No Tasker, adicione a ação **Sistema > Enviar Intent** e preencha:

| Campo do Tasker | Valor |
|---|---|
| Ação | Uma das ações da tabela abaixo |
| Cat, Tipo de Mime, Dado | Deixe como estão |
| Extra 1 | `code:SEU_CODIGO` |
| Extra 2 em diante | Conforme a ação |
| Pacote | `dev.alexcordeiro.pressvibe` |
| Destino | `Broadcast Receiver` |

Cada Extra vai no seu próprio campo, no formato `chave:valor`, sem espaço depois dos dois-pontos. Pacote e Destino ficam no fim da tela do Tasker. Role até o final e preencha os dois, senão nada acontece.

## Ações disponíveis

| O que fazer | Ação | Extras |
|---|---|---|
| Acionar botão | `dev.alexcordeiro.pressvibe.action.TRIGGER` | `button:NOME`, `input:TEXTO` (opcional) |
| Enviar mensagem | `dev.alexcordeiro.pressvibe.action.SEND` | `destination:NOME`, `title:TITULO`, `message:MENSAGEM`, `priority:NORMAL` (opcional) |
| Encerrar Ping | `dev.alexcordeiro.pressvibe.action.END_PING` | `button:NOME` (opcional, sem ele encerra todos) |
| Cancelar reenvios | `dev.alexcordeiro.pressvibe.action.CANCEL` | `button:NOME` (opcional, sem ele cancela todos) |
| Estado do botão | `dev.alexcordeiro.pressvibe.action.STATUS` | `button:NOME` |

O nome do botão precisa ser igual ao do app, inclusive maiúsculas e minúsculas. Se dois botões tiverem o mesmo nome, a tela de ajuda do app mostra o identificador interno para usar no lugar.

Na ação Enviar mensagem, a prioridade aceita `MIN`, `LOW`, `NORMAL`, `HIGH` ou `EMERGENCY`.

A ação Estado do botão devolve `idle` (parado), `sending` (enviando), `retrying` (tentando de novo) ou `ping` (Ping ativo).

## Se o app sofrer parada forçada

O Android não entrega pedidos a um app que sofreu parada forçada. Para garantir, coloque antes do Enviar Intent a ação **App > Abrir App**. Toque e segure no PressVibe e escolha a activity `automation.WakeActivity`. Ela acorda o app sem mostrar nenhuma tela.
