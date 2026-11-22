---
layout: guia
title: Envio, erros e histórico | PressVibe
description: Estados do envio, novas tentativas, mensagens de erro e histórico do PressVibe.
permalink: /apps/pressvibe/envio/
---

# Envio, erros e histórico

Quando você aciona um botão, todas as notificações dele saem em paralelo. Cada requisição tem até 15 segundos para responder. O resultado aparece no rodapé da tela principal por alguns segundos. Toque em **Detalhes** para ver o resultado de cada notificação.

Durante um envio, o mesmo botão ignora novos acionamentos. Isso evita alertas duplicados por toque repetido.

## O que cada aviso quer dizer

| Aviso | Significado | O que fazer |
|---|---|---|
| Enviando… | As requisições estão em andamento | Aguarde |
| Enviado | Todas as notificações foram aceitas | Nada |
| Enviado em parte | Parte das notificações falhou | Toque em Detalhes para ver qual |
| Erro de conexão. Nova tentativa em segundo plano. | Sem rede ou serviço fora do ar | O app tenta de novo sozinho |
| Erro de autenticação | O serviço recusou a credencial | Toque em Detalhes e depois em Editar destino |
| Recusado pelo serviço | A requisição tem algum dado inválido | Confira o destino e use Enviar teste |
| Sem destinos cadastrados | O botão não tem notificação ativa | Toque em Editar e adicione uma |
| Não entregue após 2 horas de tentativas | A rede não voltou a tempo | Avise por outro meio |

## Novas tentativas

Falhas de conexão, tempo esgotado, limite de requisições do serviço e erros do servidor entram em novas tentativas. Erros de credencial e de dados inválidos não, porque tentar de novo não resolve.

O app tenta de novo por até 2 horas a partir do acionamento. A espera entre tentativas começa em 5 segundos e dobra até 1 minuto. A mensagem que chega depois mantém os valores do momento do acionamento, como a hora e a posição.

As tentativas continuam com o app fechado e depois de reiniciar o celular. Enquanto isso, o botão mostra "Tentando…" com um anel pulsante, e o Android mostra a notificação "Tentando enviar alerta".

Para as tentativas não atrasarem com o celular parado, conceda **Sem restrição de bateria** em **Configurações > Permissões**.

## Cancelar as tentativas

Toque no botão que está em "Tentando…". O app mostra quantas notificações faltam e pergunta se você quer cancelar. Escolha **Cancelar envio** para parar ou **Continuar tentando** para manter. A confirmação existe para um toque acidental não interromper um alerta de verdade.

## Histórico

Em **Configurações > Histórico**, o app mostra os últimos 50 envios, com data, botão, destino e resultado. O histórico não guarda credenciais.

Nos alertas de Emergência do Pushover, o histórico mostra **Cancelar alerta**. Isso para a repetição do alerta no celular de quem recebe, útil quando o alarme foi falso ou a situação já se resolveu.

## Problemas comuns

### O teste funciona, mas o alerta não toca no silencioso

O PressVibe só entrega a mensagem ao serviço. Quem decide se toca no silencioso é o app do serviço no celular de quem recebe. Use prioridade Emergência no Pushover ou no ntfy e confira as configurações de notificação desses apps.

### A posição chega como "localização indisponível"

Conceda a permissão de localização em **Configurações > Permissões**. Para envios pelo widget, conceda "o tempo todo". Confira também se o GPS do celular está ligado.

### O alerta demora quando o celular está parado

Conceda **Sem restrição de bateria**. Sem ela, o Android pode adiar as novas tentativas para economizar energia.
