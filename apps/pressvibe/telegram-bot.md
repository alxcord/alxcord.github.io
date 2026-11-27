---
layout: guia
title: Criar o bot do Telegram | PressVibe
description: Passo a passo para criar um bot no Telegram com o BotFather, obter o token e o Chat ID e cadastrar o destino Telegram no PressVibe.
permalink: /apps/pressvibe/telegram-bot/
---

# Criar o bot do Telegram

O destino Telegram do PressVibe envia as mensagens por um bot seu. O bot é gratuito e é criado dentro do próprio Telegram, sem instalar nada. O processo leva uns 5 minutos.

Você vai precisar de duas informações: o **token do bot**, que identifica o bot, e o **Chat ID**, que identifica quem recebe.

## 1. Criar o bot no BotFather

1. No Telegram, procure por **@BotFather**. Use o perfil oficial, com o selo azul de verificado.
2. Toque em **Iniciar** e mande `/newbot`.
3. O BotFather pede o **nome** do bot. É o nome que aparece nas mensagens, por exemplo `PressVibe Alex`.
4. Depois ele pede o **username**. Ele precisa ser único no Telegram e terminar em `bot`, por exemplo `alex_pressvibe_bot`. Se o nome já existir, tente outro.
5. No fim, o BotFather manda uma mensagem com o **token**, no formato `123456789:ABCdefGhIJKlmnOPQrstUVwxyz`. Copie o token inteiro, com os números, os dois pontos e as letras.

Trate o token como uma senha. Quem tiver o token consegue mandar mensagens em nome do seu bot. Não publique em grupos, prints ou repositórios. Se ele vazar, mande `/revoke` para o BotFather, escolha o bot e use o token novo no PressVibe.

## 2. Iniciar a conversa com o bot

Um bot do Telegram não inicia conversa sozinho. Quem vai receber os alertas precisa falar com ele primeiro.

1. A pessoa que vai receber procura o username do bot no Telegram, ou abre o link `t.me/username_do_bot`.
2. Ela toca em **Iniciar**, ou manda `/start`.

Faça isso no celular de cada pessoa que vai receber. Cada uma terá o seu próprio Chat ID.

## 3. Descobrir o Chat ID

O endereço da API do Telegram não usa o nome nem o username do bot. O token já identifica o bot. O endereço é formado assim: `https://api.telegram.org/bot`, seguido do token colado, seguido de `/getUpdates`.

Com o token de exemplo `123456789:ABCdefGhIJKlmnOPQrstUVwxyz`, o endereço fica:

```
https://api.telegram.org/bot123456789:ABCdefGhIJKlmnOPQrstUVwxyz/getUpdates
```

Confira três pontos ao montar o seu:

- a palavra `bot` fica colada no token, sem espaço, barra ou outro caractere entre eles
- o token entra sem os sinais `<` e `>` e sem a palavra `TOKEN`
- o token está inteiro, com os dois pontos

1. Depois do `/start`, abra o seu endereço no navegador.
2. A página mostra um texto em JSON. Procure o trecho `"chat":{"id":` e copie o número que vem logo depois. Esse é o Chat ID.

Exemplo do trecho:

```json
"chat": {
  "id": 987654321,
  "first_name": "Maria",
  "type": "private"
}
```

### Se não aparecer o Chat ID

| O que a página mostra | Causa | Como resolver |
|---|---|---|
| `{"ok":true,"result":[]}` | Nenhuma mensagem nova para o bot | Mande `/start` ou outra mensagem para o bot e recarregue a página. O Telegram guarda essas mensagens por até 24 horas |
| `{"ok":false,"error_code":401,...}` | Token errado ou incompleto | Copie o token de novo do BotFather e confira os três pontos acima |
| `{"ok":false,"error_code":404,...}` | Endereço mal montado | Confira se a palavra `bot` está colada no token e se o final é `/getUpdates` |
| `{"ok":false,"error_code":409,...}` | O bot tem um webhook ativo, e o `getUpdates` não funciona com webhook | Abra `https://api.telegram.org/botTOKEN/deleteWebhook` com o seu token e tente o `getUpdates` de novo |

## 4. Cadastrar o destino no PressVibe

1. Abra **Configurações > Destinos** e crie um destino do tipo **Telegram**.
2. Preencha **Token do bot** e **Chat ID**.
3. Dê um nome fácil, por exemplo "Telegram da Maria".
4. Toque em **Enviar teste**. A mensagem "Mensagem de teste do PressVibe" deve chegar na conversa com o bot.

## Avisar um grupo

O mesmo bot manda mensagens para um grupo inteiro.

1. Adicione o bot ao grupo como participante.
2. No grupo, mande `/start@username_do_bot`. Por padrão, o bot num grupo só enxerga comandos e mensagens que o mencionam, então uma mensagem comum não aparece no `getUpdates`.
3. Abra o endereço do `getUpdates` de novo e procure o `"chat":{"id":` do grupo, com `"type":"group"` ou `"type":"supergroup"`.

O Chat ID de um grupo é negativo, por exemplo `-1001234567890`. Copie com o sinal de menos.

## Limite do Telegram em emergências

O Telegram não tem prioridade de emergência. A mensagem do bot segue as configurações de notificação do celular de quem recebe e fica muda no silencioso ou no Não perturbe.

Quem recebe melhora a chance de ver o alerta assim: na conversa com o bot, tocar no nome do bot, ligar as notificações e escolher um som próprio. E nas configurações do Android, permitir o Telegram no Não perturbe.

Mesmo assim, use o Telegram como canal extra. Para o alerta tocar no silencioso, coloque no mesmo botão um destino Pushover ou ntfy. Veja [Pushover tocando no silencioso](../pushover-silencioso/) e [ntfy tocando no silencioso](../ntfy-silencioso/).

## Personalizar o bot (opcional)

No BotFather, com o comando `/mybots`, você escolhe o bot e muda a foto, a descrição e o nome. Uma foto e uma descrição como "Alertas do PressVibe" ajudam quem recebe a reconhecer a conversa.

Veja também: [Destinos](../destinos/) e [Botões e notificações](../botoes/).
