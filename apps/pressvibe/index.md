---
layout: guia
title: PressVibe
description: Guia de uso do PressVibe, app Android para pedir ajuda com um botão.
permalink: /apps/pressvibe/
---

# PressVibe

O PressVibe é um app Android para pedir ajuda com rapidez. Você segura um botão e o app envia uma ou mais notificações push para quem você escolheu, pelo Pushover, ntfy, Telegram, Pushbullet, Simplepush ou um webhook seu.

O gesto de segurar evita envios acidentais. Nos serviços com prioridade, um alerta de emergência toca no celular de quem recebe mesmo em modo silencioso, desde que o app desse serviço esteja configurado para isso.

## Como funciona

O app trabalha com três peças. O **destino** é um serviço de envio com as suas credenciais, por exemplo "Pushover da família". O **botão** é o que você aperta na tela, com nome, ícone, cor e tamanho. A **notificação** liga um botão a um destino e define título, mensagem e prioridade.

Um botão pode ter várias notificações, e um mesmo destino serve a vários botões. O botão "Preciso de ajuda" e o botão "Cheguei bem" usam o mesmo Pushover, um com prioridade de emergência e o outro com prioridade normal.

## Recursos

| Recurso | O que faz |
|---|---|
| Toque e segura | Envia depois de segurar o botão de 0 a 5 segundos |
| Prompt interativo | Abre um campo de texto e envia o que você digitar |
| Macros | Colocam data, hora, bateria e posição GPS na mensagem |
| Widget | Aciona um botão direto da tela inicial |
| Ping | Continua enviando a sua posição de tempos em tempos depois do alerta |
| Envio persistente | Tenta de novo por até 2 horas se a rede falhar |
| Automação | Deixa o Tasker acionar botões sem conhecer as suas chaves |
| Backup | Exporta e importa tudo em um arquivo cifrado com senha |

O app tem interface em português, inglês e espanhol e funciona a partir do Android 8.0.

## Guias

Comece pelos [Primeiros passos](primeiros-passos/). Depois, use os guias conforme a necessidade.

- [Primeiros passos](primeiros-passos/): do primeiro destino ao primeiro alerta, em 5 minutos.
- [Destinos](destinos/): como obter as credenciais de cada serviço.
- [Botões e notificações](botoes/): aparência, modos de acionamento e prioridades.
- [Macros](macros/): data, hora, bateria, GPS e texto digitado na mensagem.
- [Widget](widget/): o botão na tela inicial.
- [Ping](ping/): acompanhamento da posição depois do alerta.
- [Envio, erros e histórico](envio/): o que cada aviso quer dizer.
- [Automação com Tasker](automacao/): acionar botões por outros apps.
- [Backup](backup/): levar a configuração para outro celular.
- [Privacidade](privacidade/): o que o app faz com os seus dados.

## Privacidade em uma frase

O PressVibe não tem servidor, conta nem telemetria. Tudo fica cifrado no seu celular e as mensagens vão direto para os serviços que você cadastrou.
