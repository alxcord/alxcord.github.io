---
layout: guia
title: Macros | PressVibe
description: Macros de data, hora, bateria, GPS e texto digitado nas mensagens do PressVibe.
permalink: /apps/pressvibe/macros/
---
{% raw %}

# Macros

Macros são marcadores entre chaves duplas, como `{{time}}`. No momento do envio, o app troca cada macro pelo valor real. Elas funcionam no título, na mensagem e no corpo do webhook.

O app resolve as macros uma vez por acionamento. Todas as notificações do mesmo botão recebem os mesmos valores.

## Lista de macros

| Macro | Valor | Exemplo |
|---|---|---|
| `{{date}}` | Data local | 13/11/2026 |
| `{{time}}` | Hora local | 21:19 |
| `{{datetime}}` | Data e hora locais | 13/11/2026 21:19 |
| `{{timestamp}}` | Data e hora no padrão ISO 8601, com fuso | 2026-11-13T21:19:00-03:00 |
| `{{lat}}` | Latitude | -23.96083 |
| `{{lon}}` | Longitude | -46.33361 |
| `{{accuracy}}` | Precisão da posição, em metros | 12 |
| `{{maps_url}}` | Link do Google Maps para a posição | https://maps.google.com/?q=-23.96083,-46.33361 |
| `{{button}}` | Ícone e nome do botão | 🆘 Preciso de ajuda |
| `{{battery}}` | Nível da bateria, em porcentagem | 37 |
| `{{input}}` | Texto digitado no Prompt interativo | Pneu furou |

No webhook customizado, valem também `{{title}}` e `{{message}}`, com o título e a mensagem já resolvidos.

## Regras

Data e hora seguem o formato do idioma do app. Em inglês, `{{date}}` sai como 11/13/2026.

No modo Toque e segura e no widget, `{{input}}` vira texto vazio.

Uma macro escrita errado, como `{{hora}}`, fica no texto do jeito que foi escrita. Confira na **Prévia** antes de salvar.

## Posição GPS

As macros `{{lat}}`, `{{lon}}`, `{{accuracy}}` e `{{maps_url}}` usam a localização do celular.

O app pede a permissão de localização quando você salva uma notificação com uma dessas macros. No envio, ele usa a última posição conhecida, se tiver até 2 minutos. Se não tiver, pede uma posição nova e espera até 5 segundos.

Sem posição ou sem permissão, essas macros viram o texto "localização indisponível". O alerta sai do mesmo jeito. A falta de GPS nunca bloqueia um envio.

Para o widget enviar a posição com o app fechado, o Android exige a permissão de localização "o tempo todo". Veja [Widget](../widget/).

## Mensagens prontas

Pedido de socorro com posição e bateria:

```
Preciso de ajuda. {{datetime}}
Posição: {{maps_url}} (precisão {{accuracy}} m)
Bateria: {{battery}}%
```

Aviso de chegada:

```
Cheguei bem às {{time}}.
```

Prompt com contexto:

```
{{input}}
Enviado às {{time}} de {{maps_url}}
```
{% endraw %}
