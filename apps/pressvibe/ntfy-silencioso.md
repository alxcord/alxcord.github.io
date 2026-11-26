---
layout: guia
title: ntfy tocando no silencioso | PressVibe
description: Como configurar o app ntfy de quem recebe para o alerta do PressVibe tocar mesmo com o celular no silencioso ou no vibrar.
permalink: /apps/pressvibe/ntfy-silencioso/
---

# ntfy tocando no silencioso

Este guia é para quem **recebe** os alertas pelo ntfy. A configuração é feita no celular dessa pessoa, no app ntfy. O PressVibe só precisa mandar com a prioridade certa.

Com tudo configurado, o alerta de emergência toca como um despertador: usa o volume do alarme, ignora o modo silencioso e o vibrar, e repete até a pessoa dispensar a notificação.

## Como funciona

O Android controla o som de notificações e o som de alarmes de forma separada. No silencioso ou no vibrar, as notificações ficam mudas, mas o despertador continua tocando.

O app ntfy tem a opção **Continuar alertando na prioridade máxima** (no app em inglês, *Keep alerting for highest priority*). Com ela ligada, mensagens de prioridade máxima tocam pelo canal de alarme do Android, como um despertador, e repetem até a notificação ser dispensada.

## No PressVibe (quem envia)

Na notificação do botão, use o destino ntfy com a prioridade **Emergência**. O PressVibe envia isso como prioridade 5, a máxima do ntfy. As outras prioridades não tocam como alarme.

## No celular de quem recebe

1. Instale o app ntfy e assine o mesmo tópico configurado no destino do PressVibe.
2. Abra o tópico, toque no menu e entre nas configurações da inscrição. Ligue **Continuar alertando na prioridade máxima**. Se a opção estiver em "usar configuração global", ligue também a opção geral em **Configurações** do app.
3. Deixe o som de notificação do ntfy em um **som do sistema**. Com um arquivo de som personalizado, o ntfy não consegue tocar pelo canal de alarme e o alerta fica mudo no silencioso. É um problema conhecido do app ntfy.
4. Libere o ntfy no **Não perturbe**. Nas configurações do Android, abra Notificações, depois Não perturbe (em alguns celulares, Modos), e adicione o ntfy aos apps permitidos. Confira também se os alarmes estão permitidos no Não perturbe.
5. Deixe o **volume do alarme** alto. É ele que controla o volume do alerta, e não o volume de notificação ou de toque.
6. Desative a otimização de bateria do ntfy: Configurações do Android, Apps, ntfy, Bateria, **Sem restrições**. Assim o Android não atrasa a entrega com a tela desligada.

## Teste antes de precisar

Faça o teste com o botão real, com prioridade Emergência, em três situações no celular de quem recebe:

| Situação do celular | Resultado esperado |
|---|---|
| Som normal | Toca e repete até dispensar |
| Vibrar | Toca no volume do alarme |
| Silencioso ou Não perturbe | Toca no volume do alarme |

Se não tocar em alguma delas, revise os passos 3 a 5. Alguns fabricantes alteram o comportamento do som de alarme. Se o seu celular for um desses, use também o Pushover no mesmo botão, como recomendado no [guia inicial](../).

Veja também: [Destinos](../destinos/) e [Botões e notificações](../botoes/).
