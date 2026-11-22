---
layout: guia
title: Botões e notificações | PressVibe
description: Aparência, modos de acionamento, notificações e prioridades dos botões do PressVibe.
permalink: /apps/pressvibe/botoes/
---

# Botões e notificações

Os botões ficam na tela principal. Cada botão tem uma aparência, um modo de acionamento e uma lista de notificações. Para gerenciar, abra **Configurações > Botões**. Ali você cria, edita, duplica, exclui e muda a ordem com **Mover para cima** e **Mover para baixo**. O app aceita até 12 botões.

## Aparência

| Campo | Opções |
|---|---|
| Nome | Texto livre |
| Ícone | Um de 24 emojis, como 🆘 🚨 🏥 🚗 📍 |
| Cor | 11 cores. A cor do texto se ajusta sozinha para ficar legível |
| Tamanho | Pequeno, Médio ou Grande |

O botão precisa de nome, de ícone ou dos dois.

Os botões são redondos e ficam em uma grade de uma ou duas colunas, na ordem que você definiu. Dois botões seguidos do mesmo tamanho dividem a linha. Um botão Grande ocupa a linha sozinho. Com muitos botões, a tela rola.

Se você girar o celular, a grade não muda de lugar. Só o ícone e o nome de cada botão giram para ficar de pé. Assim você acha o botão no mesmo lugar sempre.

## Modos de acionamento

### Toque e segura

Você mantém o dedo no botão e um anel cresce em volta dele. Quando o anel fecha, o celular vibra e o alerta sai. Se você soltar antes, nada é enviado.

O **Tempo de acionamento** vai de 0 a 5 segundos, em passos de meio segundo. O padrão é 2 segundos. Com 0, um toque simples já envia. Use 0 só em botões sem risco, como "Cheguei bem".

### Prompt interativo

Um toque abre uma janela com um campo de texto. O texto digitado entra na mensagem pela macro `{{input}}`. O botão **Enviar** só fica ativo com algum texto escrito.

Use esse modo quando o contexto importa, como "Pneu furou na estrada" ou "Atrasei, chego às 22h".

## Notificações do botão

Cada notificação é um envio. Um botão pode ter várias, para avisar pessoas diferentes ou usar serviços diferentes ao mesmo tempo. Todas saem em paralelo, e a falha de uma não impede as outras.

| Campo | Observação |
|---|---|
| Destino | Um dos [destinos](../destinos/) cadastrados |
| Título | Aceita macros |
| Mensagem | Aceita macros. Toque em uma macro da lista para inseri-la |
| Prioridade | Só aparece para Pushover e ntfy |
| Som | Só no Pushover. Nome de um som do Pushover, opcional |
| Tags | Só no ntfy. Separadas por vírgula. Tags com nome de emoji, como `warning`, viram ícone na notificação |
| Ativa | Liga ou desliga a notificação sem apagar |

A tela mostra uma **Prévia** do título e da mensagem com as macros resolvidas.

## Prioridades

O app usa cinco níveis e traduz cada um para o valor do serviço.

| Nível | Pushover | ntfy | Uso sugerido |
|---|---|---|---|
| Mínima | -2 | 1 | Registro, sem som |
| Baixa | -1 | 2 | Aviso discreto |
| Normal | 0 | 3 | "Cheguei bem" |
| Alta | 1 | 4 | Algo urgente |
| Emergência | 2 | 5 | Pedido de socorro |

No Pushover, a prioridade Emergência repete o alerta até alguém confirmar. Dois campos controlam isso:

| Campo | Padrão | Limite |
|---|---|---|
| Repetir a cada (s) | 60 | Mínimo de 30 segundos |
| Expirar em (s) | 3600 | Máximo de 10800 segundos (3 horas) |

Para parar a repetição pelo seu lado, abra **Configurações > Histórico** e toque em **Cancelar alerta** no envio correspondente.

## Exemplos de botões

| Botão | Modo | Notificações |
|---|---|---|
| 🆘 Preciso de ajuda | Toque e segura, 2 s | Pushover Emergência com `{{maps_url}}` e Telegram para o grupo da família |
| ✅ Cheguei bem | Toque e segura, 0 s | ntfy Normal com `{{time}}` |
| 🚗 Problema no carro | Prompt interativo | Pushover Alta com `{{input}}` e `{{maps_url}}` |
