---
layout: guia
title: Backup | PressVibe
description: Como exportar e importar a configuração do PressVibe.
permalink: /apps/pressvibe/backup/
---

# Backup

O PressVibe fica fora do backup automático do Android, para as suas credenciais não irem para a nuvem. Por isso, ao trocar de celular, você leva a configuração com um arquivo de backup próprio, cifrado com uma senha sua.

## Exportar

1. Abra **Configurações** e role até **Exportar configurações**.
2. Crie uma senha com pelo menos 12 caracteres e repita a senha.
3. Escolha onde salvar o arquivo `.pvbackup`.

O app mostra a força da senha. Uma senha longa com letras, números e símbolos fica forte.

> A senha não pode ser recuperada. Sem ela, o arquivo não abre. Guarde a senha em um gerenciador de senhas.

O arquivo leva os botões, os destinos com as credenciais e as notificações. A cifragem usa AES-256-GCM, com a chave derivada da senha por Argon2id.

## Importar

1. No celular novo, abra **Configurações > Importar configurações**.
2. Toque em **Abrir** e escolha o arquivo.
3. Digite a senha.
4. O app mostra quantos botões e destinos o backup tem. Confirme em **Substituir**.

A importação troca todos os botões, destinos e chaves do aparelho pelos do backup. Algumas coisas ficam como estão no aparelho: as permissões, o aceite do aviso de privacidade e o código de integração da automação, para as suas automações não pararem.

## Erros na importação

| Mensagem | Causa |
|---|---|
| Senha errada ou arquivo danificado. Nada foi alterado. | A senha não confere ou o arquivo foi modificado |
| Este backup foi feito por uma versão mais nova do app. Nada foi alterado. | Atualize o PressVibe e tente de novo |
| Este arquivo não é um backup do PressVibe. Nada foi alterado. | O arquivo escolhido é outro |

Em todos os casos de erro, a configuração atual fica intacta.
