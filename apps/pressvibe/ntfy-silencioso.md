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

O app ntfy tem uma opção que faz as mensagens de prioridade máxima tocarem pelo canal de alarme do Android, como um despertador, e repetirem até a notificação ser dispensada.

## No PressVibe (quem envia)

Na notificação do botão, use o destino ntfy com a prioridade **Emergência**. O PressVibe envia isso como prioridade 5, a **Prioridade máxima** do ntfy. As outras prioridades não tocam como alarme.

## No celular de quem recebe

Os nomes abaixo são os do app ntfy em português. Nas telas do Android, o texto e o caminho dos menus mudam conforme o fabricante, a versão do Android e o idioma do aparelho. Se não achar uma opção com o mesmo nome, procure a de sentido parecido. A busca das Configurações do Android também ajuda: digite "Não perturbe", "Modos" ou "Bateria".

### No app ntfy

1. Instale o app ntfy e assine o mesmo tópico configurado no destino do PressVibe.
2. Abra o tópico, toque no menu e entre nas configurações da inscrição.
3. Ligue **Entrega instantânea**. Sem ela, as mensagens chegam pelo Firebase e a entrega pode demorar. Com ela, o app mantém uma conexão aberta e o alerta chega na hora, com um consumo pequeno de bateria.
4. Toque em **Mantenha o alerta para a prioridade mais alta** e escolha **Continuar alertando**. É a opção que faz o alerta tocar como despertador e repetir até ser dispensado.
5. Ligue **Configuração de notificações personalizadas**. Assim os ajustes de som e Não perturbe valem só para este tópico.
6. Toque em **Configurar configurações de notificação**. O Android abre a tela de notificações do ntfy, com uma categoria para cada prioridade do tópico. Entre em **Prioridade máxima** e confira:
   - **Mostrar notificações** ligado
   - **Som** com um som do sistema. Com um arquivo de som personalizado, o ntfy não consegue tocar pelo canal de alarme e o alerta fica mudo no silencioso. É um problema conhecido do app ntfy.
   - a opção de ignorar ou sobrepor o **Não perturbe** ligada, se ela aparecer nessa tela. Em alguns aparelhos ela não aparece aqui, e o ajuste é feito no passo 7.

### Nas configurações do Android

7. Abra o Não perturbe (em alguns celulares, Modos, Foco ou Modo silencioso). Adicione o ntfy aos apps permitidos e confira se os **alarmes** estão permitidos.
8. Deixe o **volume do alarme** alto. É ele que controla o volume do alerta, e não o volume de notificação ou de toque.
9. Tire o ntfy da otimização de bateria. No Android padrão, o caminho é Configurações, Apps, ntfy, Bateria, **Sem restrições**. Em outros aparelhos a opção pode se chamar "Não otimizar", "Sem restrições" ou "Permitir atividade em segundo plano". Assim o Android não fecha o ntfy com a tela desligada.

## Teste antes de precisar

Faça o teste com o botão real, com prioridade Emergência, em três situações no celular de quem recebe:

| Situação do celular | Resultado esperado |
|---|---|
| Som normal | Toca e repete até dispensar |
| Vibrar | Toca no volume do alarme |
| Silencioso ou Não perturbe | Toca no volume do alarme |

Se não tocar em alguma delas, revise os passos 4 a 8. Alguns fabricantes alteram o comportamento do som de alarme. Se o seu celular for um desses, use também o Pushover no mesmo botão, como recomendado no [guia inicial](../).

Veja também: [Destinos](../destinos/) e [Botões e notificações](../botoes/).
