---
layout: guia
title: Primeiros passos | PressVibe
description: Configure o PressVibe e envie o primeiro alerta.
permalink: /apps/pressvibe/primeiros-passos/
---
{% raw %}

# Primeiros passos

Este guia leva você do app recém-instalado até o primeiro alerta enviado. O exemplo usa o ntfy, que é gratuito e não pede cadastro. Para outros serviços, veja [Destinos](../destinos/).

## 1. Prepare quem vai receber

No celular de quem vai receber o alerta, instale o app ntfy pela Play Store. Toque em **+**, escolha um nome de tópico difícil de adivinhar, como `familia-silva-7k3q9`, e confirme. Anote esse nome.

> No servidor público ntfy.sh, qualquer pessoa que souber o nome do tópico lê as mensagens. Por isso o nome precisa ser longo e aleatório.

## 2. Abra o PressVibe pela primeira vez

Na primeira abertura, o app mostra um aviso de privacidade e, em seguida, explica cada permissão. Todas são opcionais. O app funciona sem elas, com limitações.

| Permissão | Sem ela |
|---|---|
| Notificações | O envio funciona, mas você só vê o andamento dentro do app |
| Localização | Os alertas com posição dizem "localização indisponível" |
| Localização o tempo todo | Os alertas com posição enviados pelo widget saem sem posição |
| Sem restrição de bateria | As novas tentativas de envio podem atrasar com o celular parado |

Para um app de emergência, conceda todas. Você revê as permissões depois em **Configurações > Permissões**.

## 3. Cadastre o destino

1. Toque no ícone de engrenagem e abra **Destinos**.
2. Toque em **+**.
3. Dê um nome, por exemplo "ntfy da família", e escolha o serviço **ntfy**.
4. Deixe a URL do servidor como está (`https://ntfy.sh`) e preencha o **Tópico** com o nome que você anotou.
5. Toque em **Enviar teste**. A mensagem de teste deve chegar no outro celular.
6. Toque em **Salvar**.

## 4. Crie o botão

1. Volte para **Configurações** e abra **Botões**.
2. Toque em **+**.
3. Escreva o nome "Preciso de ajuda", escolha o ícone 🆘 e a cor vermelha.
4. Deixe a interação em **Toque e segura** e o tempo de acionamento em 2 segundos.
5. Toque em **Adicionar notificação** e escolha o destino "ntfy da família".
6. No título, escreva `{{button}}`. Na mensagem, escreva `Preciso de ajuda. Estou aqui: {{maps_url}}`.
7. Escolha a prioridade **Emergência** e salve.

A tela de edição mostra uma prévia com as macros resolvidas. As macros estão explicadas em [Macros](../macros/).

## 5. Envie o primeiro alerta

Volte à tela principal e segure o botão. Um anel cresce em volta dele. Ao fechar o círculo, o celular vibra e o alerta sai. Se você soltar antes, nada é enviado.

O resultado aparece no rodapé da tela. Toque em **Detalhes** para ver o resultado de cada notificação.

## Próximos passos

Coloque o botão na tela inicial com o [Widget](../widget/). Para mandar notificações periódicas depois do alerta, com a sua posição se você colocar a macro na mensagem, ligue o [Ping](../ping/). Para não perder a configuração ao trocar de celular, faça um [Backup](../backup/).
{% endraw %}
