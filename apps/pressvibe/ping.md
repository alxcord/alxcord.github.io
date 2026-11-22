---
layout: guia
title: Ping | PressVibe
description: Notificações periódicas depois de um alerta do PressVibe.
permalink: /apps/pressvibe/ping/
---
{% raw %}

# Ping

O Ping continua enviando notificações de tempos em tempos depois do alerta, até você encerrar. O uso mais comum é deixar quem recebe acompanhar onde você está.

O Ping manda só o que está escrito nas mensagens dele. A posição e a bateria entram apenas se você colocar as macros `{{maps_url}}` e `{{battery}}` no texto. Sem informações que mudam a cada envio, um aviso periódico perde o sentido, então coloque essas macros nas mensagens do Ping.

## Como ligar

1. Em **Configurações > Botões**, abra o botão.
2. Ligue o **Ping**.
3. Escolha o intervalo entre envios e a duração máxima.
4. Toque em **Adicionar notificação de Ping** e configure destino, título, mensagem e prioridade.

| Ajuste | Faixa | Padrão |
|---|---|---|
| Intervalo | 1 a 60 minutos | 3 minutos |
| Duração máxima | 1 a 12 horas | 2 horas |

As notificações do Ping são separadas das notificações do alerta. Use prioridade Baixa ou Normal nelas, para não tocar como emergência a cada poucos minutos.

Uma mensagem típica de Ping:

```
Posição atual: {{maps_url}}
Bateria: {{battery}}% às {{time}}
```

## Como funciona

O primeiro Ping sai um intervalo depois do alerta. A cada envio, o app resolve de novo as macros da mensagem. Se ela usa posição, bateria ou hora, esses valores saem atualizados.

Enquanto o Ping está ativo, o botão mostra "Ping ativo" com um anel que pulsa devagar, e o rodapé da tela mostra quantos Pings estão rodando. O Ping continua mesmo com o app fechado.

Se um envio de Ping falhar, o app não tenta de novo. O próximo Ping, com valores mais novos, toma o lugar dele.

## Como encerrar

Toque no botão com "Ping ativo" e confirme **Encerrar Ping**. Os destinos do Ping recebem uma última mensagem dizendo como ele terminou.

| Motivo | Mensagem final |
|---|---|
| Você encerrou | Ping encerrado pelo usuário. |
| Uma automação encerrou | Ping encerrado por uma automação. |
| Acabou a duração máxima | Ping encerrado: duração máxima atingida. |

O Ping nunca roda sem prazo. No limite de tempo que você definiu, de no máximo 12 horas, ele para sozinho.

## O Ping não é rastreamento contínuo

O Ping envia a cada intervalo, de 1 minuto a 1 hora. Entre um envio e outro, quem recebe não sabe onde você está. Use o Ping como reforço e, numa situação de risco, compartilhe também a localização em tempo real pelo WhatsApp ou pelo Google Maps. O PressVibe depende de serviços de terceiros e não garante a entrega, então quanto mais canais, melhor.
{% endraw %}
