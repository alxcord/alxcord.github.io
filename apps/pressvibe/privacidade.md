---
layout: guia
title: Política de Privacidade | PressVibe
description: Política de privacidade do app PressVibe.
permalink: /apps/pressvibe/privacidade/
---

# Política de Privacidade

Última atualização: 22 de novembro de 2026

Esta política explica quais dados o app PressVibe usa e como eles são tratados. O PressVibe é um app Android para pedir ajuda com rapidez. Você pressiona um botão e o app envia notificações push pelos serviços que você mesmo configura.

## 1. Responsável

Alex Cordeiro, desenvolvedor do PressVibe.

Contato: [support@alexcordeiro.dev](mailto:support@alexcordeiro.dev)

## 2. Resumo

O desenvolvedor não coleta, não recebe e não armazena nenhum dado seu. O app não tem conta de usuário, servidor próprio, sincronização em nuvem, anúncios nem ferramentas de análise ou rastreamento. Tudo o que você configura fica só no seu aparelho, cifrado. O app só se comunica com os serviços de notificação que você cadastrou.

## 3. Dados que ficam no seu aparelho

O app guarda no aparelho os destinos que você cadastra, com as credenciais de cada serviço, os botões e as notificações que você configura, e o histórico dos últimos 50 envios, com data, botão, destino e resultado. O histórico não guarda credenciais.

A configuração, as credenciais, os envios pendentes e os Pings em andamento ficam em arquivos cifrados com AES-GCM. A chave fica no Android Keystore. O app fica fora do backup automático do Android, então esses dados não vão para o Google Drive nem para outro aparelho.

Para apagar esses dados, desinstale o app ou limpe os dados dele nas configurações do Android.

## 4. Dados que o app envia

Quando você aciona um botão, o app envia a mensagem para o serviço que você escolheu. A mensagem contém o título e o texto que você definiu e, se você usar macros, valores como data, hora, nível de bateria, o texto que você digitou e a localização.

Os serviços aceitos são Pushover, ntfy, Telegram, Pushbullet, Simplepush e webhook customizado. O envio vai direto do seu aparelho para o serviço, por HTTPS. No webhook customizado, o app pede sua confirmação antes de usar HTTP sem cifragem.

O desenvolvedor não participa desse caminho e não tem acesso às mensagens. Cada serviço trata os dados conforme a própria política de privacidade:

- Pushover: [pushover.net/privacy](https://pushover.net/privacy)
- ntfy: [ntfy.sh/docs/privacy](https://ntfy.sh/docs/privacy/)
- Telegram: [telegram.org/privacy](https://telegram.org/privacy)
- Pushbullet: [pushbullet.com/privacy](https://www.pushbullet.com/privacy)
- Simplepush: [simplepush.io](https://simplepush.io)

No ntfy e no webhook customizado, você pode usar um servidor seu. Nesse caso, quem trata os dados é você.

## 5. Localização

O app só lê a localização no momento em que um botão é acionado, e só se a mensagem desse botão usa uma macro de posição. Ele não rastreia você em segundo plano.

O envio repetido da posição só acontece com o Ping, que você liga em cada botão. O Ping para sozinho no limite de tempo que você definir, no máximo 12 horas, e você encerra quando quiser.

A posição entra no texto da mensagem e segue para o serviço que você escolheu. O app não envia a posição para nenhum outro lugar.

A permissão de localização em segundo plano é opcional e serve para o widget enviar a posição com o app fechado. Você pode negar ou retirar as permissões a qualquer momento nas configurações do Android. O envio continua funcionando, sem a posição.

## 6. Automação

Outros apps do seu aparelho, como o Tasker, só acionam o PressVibe se você ligar a automação e passar a eles o código de integração. A automação vem desligada. Os pedidos de automação não recebem credenciais nem configuração.

## 7. Backup

O backup é um arquivo que você exporta e guarda onde quiser, cifrado com uma senha sua. O desenvolvedor não recebe esse arquivo nem a senha.

## 8. Permissões

| Permissão | Para que serve |
|---|---|
| Internet | Enviar as requisições aos serviços de notificação |
| Vibração | Dar retorno ao acionar o botão |
| Notificações | Mostrar o andamento de envios pendentes e avisar falhas de entrega |
| Localização precisa | Preencher as macros de posição, quando você usa |
| Localização em segundo plano | Preencher as macros de posição nos envios pelo widget, opcional |
| Sem restrição de bateria | Manter as novas tentativas sem atraso, opcional |

## 9. Compartilhamento

O desenvolvedor não compartilha dados, porque não os recebe. O único compartilhamento é o envio que você mesmo configura, descrito na seção 4.

## 10. Crianças

O app não é direcionado a menores de 13 anos. Como o app não coleta dados, não há tratamento de dados de crianças pelo desenvolvedor.

## 11. Seus direitos

Como o desenvolvedor não guarda dados seus, não há dados para acessar, corrigir ou excluir na nossa base. Você controla tudo no próprio aparelho. Para dúvidas ou para exercer qualquer direito previsto na Lei Geral de Proteção de Dados (Lei 13.709/2018), escreva para [support@alexcordeiro.dev](mailto:support@alexcordeiro.dev).

## 12. Segurança

As credenciais ficam cifradas no aparelho, com chave no Android Keystore. Os campos de credencial aparecem mascarados na tela. Todas as chamadas usam HTTPS. O histórico de envios não guarda credenciais.

## 13. Mudanças nesta política

Se o app passar a tratar dados de outra forma, esta política será atualizada antes da nova versão e a data no topo será alterada.
