---
layout: guia
title: PressVibe
description: Guia de uso do PressVibe, app Android que manda alertas capazes de tocar no celular de quem recebe mesmo no modo silencioso.
permalink: /apps/pressvibe/
---

# PressVibe

O PressVibe nasceu de um problema comum: uma mensagem importante chega e ninguém vê, porque o celular de quem recebe está no silencioso. O app foi feito para quebrar essa barreira. Você segura um botão e ele manda alertas que, configurados com prioridade de emergência, tocam no celular de quem recebe mesmo no modo silencioso.

Os alertas saem por serviços de notificação como Pushover, ntfy, Telegram, Pushbullet, Simplepush ou um webhook seu. O gesto de segurar o botão evita envios acidentais.

## Leia antes de confiar uma emergência ao app

O PressVibe depende de serviços de terceiros, da rede do seu celular e da configuração do celular de quem recebe. Ele não tem como garantir que o alerta chegue em todas as situações.

Numa situação de perigo, quanto mais canais, melhor. Siga estas recomendações:

1. **Use vários destinos em cada botão.** Se um serviço falhar, os outros entregam. Um botão pode avisar pelo Pushover e pelo Telegram ao mesmo tempo, por exemplo.
2. **Teste o alerta com quem vai receber.** Confirme que ele toca no silencioso no celular da pessoa, e não só que a mensagem chega.
3. **Tenha contingências fora do app.** Compartilhe também a localização em tempo real pelo WhatsApp ou pelo Google Maps com as pessoas de confiança. O [Ping](ping/) do PressVibe envia de tempos em tempos e não substitui um rastreamento contínuo.

## Como funciona

O app trabalha com três peças. O **destino** é um serviço de envio com as suas credenciais, por exemplo "Pushover da família". O **botão** é o que você aperta na tela, com nome, ícone, cor e tamanho. A **notificação** liga um botão a um destino e define título, mensagem e prioridade.

Um botão pode ter várias notificações, e um mesmo destino serve a vários botões. O conteúdo de cada mensagem é você quem define. Data, hora, bateria e localização só entram quando você coloca as [macros](macros/) correspondentes no texto.

## Para que serve

O uso principal é o pedido de socorro, mas o mesmo mecanismo resolve outras situações:

| Uso | Como montar |
|---|---|
| Pedido de socorro | Botão com prioridade Emergência e a macro de localização na mensagem |
| Avisar que chegou bem | Botão de toque simples com prioridade Normal |
| Lembrar onde estacionou o carro | Botão que manda para você mesmo uma mensagem com o link do mapa |
| Avisar sozinho ao sair do carro | O Tasker aciona um botão quando o celular desconecta do Bluetooth do carro. Veja [Automação](automacao/) |
| Recado com contexto | Botão no modo Prompt, em que você digita o texto antes de enviar |

## Recursos

| Recurso | O que faz |
|---|---|
| Toque e segura | Envia depois de segurar o botão de 0 a 5 segundos |
| Prompt interativo | Abre um campo de texto e envia o que você digitar |
| Macros | Colocam data, hora, bateria e posição GPS na mensagem, quando você as usa |
| Widget | Aciona um botão direto da tela inicial |
| Ping | Repete notificações de tempos em tempos depois do alerta, até você encerrar |
| Envio persistente | Tenta de novo por até 2 horas se a rede falhar |
| Automação | Deixa o Tasker acionar botões sem conhecer as suas chaves |
| Backup | Exporta e importa tudo em um arquivo cifrado com senha |

O app tem interface em português, inglês e espanhol e funciona a partir do Android 8.0.

## Versão gratuita e versão premium

A versão gratuita tem um botão. Ele cobre o caso principal: um pedido de socorro que toca no silencioso.

A versão premium libera os demais botões, para os outros usos da tabela acima. Comprar a premium é a forma de contribuir com o desenvolvimento do app.

O PressVibe não tem e não vai ter propaganda, nem nada que atrapalhe o uso. Num app pensado para emergências, um anúncio na tela pode custar o toque que pediria ajuda.

## Guias

Comece pelos [Primeiros passos](primeiros-passos/). Depois, use os guias conforme a necessidade.

- [Primeiros passos](primeiros-passos/): do primeiro destino ao primeiro alerta, em 5 minutos.
- [Destinos](destinos/): como obter as credenciais de cada serviço.
- [Pushover tocando no silencioso](pushover-silencioso/): como quem recebe configura o app Pushover para o alerta tocar como alarme.
- [ntfy tocando no silencioso](ntfy-silencioso/): como quem recebe configura o app ntfy para o alerta tocar como despertador.
- [Botões e notificações](botoes/): aparência, modos de acionamento e prioridades.
- [Macros](macros/): data, hora, bateria, GPS e texto digitado na mensagem.
- [Widget](widget/): o botão na tela inicial.
- [Ping](ping/): notificações periódicas depois do alerta.
- [Envio, erros e histórico](envio/): o que cada aviso quer dizer.
- [Automação com Tasker](automacao/): acionar botões por outros apps.
- [Backup](backup/): levar a configuração para outro celular.
- [Privacidade](privacidade/): o que o app faz com os seus dados.

## Privacidade em uma frase

O PressVibe não tem servidor, conta, telemetria nem propaganda. Tudo fica cifrado no seu celular e as mensagens vão direto para os serviços que você cadastrou.
