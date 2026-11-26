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

O app ntfy tem a opção **Mantenha o alerta para a prioridade mais alta**. Com ela ligada, mensagens de prioridade máxima tocam pelo canal de alarme do Android, como um despertador, e repetem até a notificação ser dispensada.

## No PressVibe (quem envia)

Na notificação do botão, use o destino ntfy com a prioridade **Emergência**. O PressVibe envia isso como prioridade 5, a máxima do ntfy. As outras prioridades não tocam como alarme.

## No celular de quem recebe

1. Instale o app ntfy e assine o mesmo tópico configurado no destino do PressVibe.
2. Abra o tópico, toque no menu e entre nas configurações da inscrição.
3. Ligue **Configuração de notificações personalizadas**. Assim as opções abaixo valem só para este tópico e não mudam os outros.
4. Toque em **Mantenha o alerta para a prioridade mais alta** e ative a opção.
5. Toque em **Configurar configurações de notificação** (Ignorar o Não Perturbe, sons, etc.). O Android abre as configurações de notificação do tópico. Na categoria de prioridade máxima:
   - ative **Ignorar o Não Perturbe**
   - deixe o som em um **som do sistema**. Com um arquivo de som personalizado, o ntfy não consegue tocar pelo canal de alarme e o alerta fica mudo no silencioso. É um problema conhecido do app ntfy.
6. Nas configurações do Android, abra o Não perturbe (em alguns celulares, Modos) e confira se os **alarmes** estão permitidos.
7. Deixe o **volume do alarme** alto. É ele que controla o volume do alerta, e não o volume de notificação ou de toque.
8. Desative a otimização de bateria do ntfy: Configurações do Android, Apps, ntfy, Bateria, **Sem restrições**. Assim o Android não atrasa a entrega com a tela desligada.

## Teste antes de precisar

Faça o teste com o botão real, com prioridade Emergência, em três situações no celular de quem recebe:

| Situação do celular | Resultado esperado |
|---|---|
| Som normal | Toca e repete até dispensar |
| Vibrar | Toca no volume do alarme |
| Silencioso ou Não perturbe | Toca no volume do alarme |

Se não tocar em alguma delas, revise os passos 4 a 7. Alguns fabricantes alteram o comportamento do som de alarme. Se o seu celular for um desses, use também o Pushover no mesmo botão, como recomendado no [guia inicial](../).

Veja também: [Destinos](../destinos/) e [Botões e notificações](../botoes/).
