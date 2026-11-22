---
layout: guia
title: Widget | PressVibe
description: Como usar o widget de tela inicial do PressVibe.
permalink: /apps/pressvibe/widget/
---
{% raw %}

# Widget

O widget coloca um botão do PressVibe na tela inicial. O envio acontece em segundo plano, sem abrir o app.

## Como adicionar

1. No PressVibe, abra **Configurações > Botão do widget** e escolha o botão.
2. Na tela inicial do Android, toque e segure em uma área vazia e escolha **Widgets**.
3. Procure o **PressVibe** ("Um botão com contagem") e arraste para a tela.

O widget usa a cor, o ícone e o nome do botão escolhido. Se nenhum botão estiver escolhido, ele mostra "Escolha um botão no app".

## Como acionar

O Android não deixa um widget detectar o gesto de segurar. Por isso, no widget, o segurar vira uma contagem.

1. Toque uma vez no widget. A contagem começa e o progresso aparece no próprio widget.
2. Para cancelar, toque de novo durante a contagem ("Toque para cancelar").
3. No fim da contagem, o celular vibra e o alerta sai.

A duração da contagem é o tempo de acionamento do botão, de 0 a 5 segundos. Com 0, o toque envia na hora.

Depois do envio, o widget mostra o resultado por alguns segundos e volta ao estado inicial.

## Diferenças em relação ao app

O widget nunca abre o campo de texto, mesmo se o botão estiver no modo Prompt interativo. Nesse caso, `{{input}}` sai vazio. Para botões de widget, prefira mensagens que não dependem de texto digitado.

Para as macros de GPS funcionarem pelo widget, conceda a permissão de localização **o tempo todo** em **Configurações > Permissões**. Sem ela, o widget usa a última posição conhecida pelo app ou envia "localização indisponível".

> O PressVibe só lê a localização no momento de um envio cuja mensagem usa uma macro de posição, mesmo com a permissão "o tempo todo". Ele não rastreia você em segundo plano.
{% endraw %}
