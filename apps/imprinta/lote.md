---
layout: guia
app: imprinta
title: Variáveis e lote | Imprinta
description: Variáveis e impressão em lote no Imprinta, a partir de lista, CSV ou planilha do Google.
permalink: /apps/imprinta/lote/
---

# Variáveis e lote

As variáveis colocam valores do momento dentro de um texto, do QR code ou do código de barras. A impressão em lote usa essas variáveis para imprimir uma etiqueta diferente por linha de uma lista.

## Variáveis

Toque em **+ Variável**, ao lado de cada campo que aceita variável, para ver a lista e inserir.

| Variável | O que vira |
|---|---|
| `{today}` | Data da impressão, no formato da Personalização. Aceita formato próprio: `{today:dd/MM}` |
| `{time}` | Hora da impressão. Aceita formato próprio: `{time:HH:mm:ss}` |
| `{seq}` | Posição na sequência do lote. Fora de um lote, vale 1. Com zeros à esquerda: `{seq:3}` vira 001 |
| `{total}` | Quantas etiquetas tem o lote. Fora de um lote, vale 1 |
| `{col1}`, `{col2}`… | Valor da coluna da linha, pela posição. Só dentro de um lote |
| `{nome-da-coluna}` | Valor da coluna pelo nome do cabeçalho. Só dentro de um lote |

Fora de um lote, as colunas saem em branco.

## Impressão em lote

Na tela de impressão, toque em **Imprimir em lote** e escolha a fonte da lista:

| Fonte | Como funciona |
|---|---|
| Colar lista | Uma linha por etiqueta |
| Arquivo CSV | Um arquivo do celular. A primeira linha pode ter os nomes das colunas |
| Planilha do Google | Cole o link de compartilhamento da planilha |

Antes de imprimir, a revisão mostra quantas linhas o lote tem, o número de cada sequência e uma prévia de cada etiqueta. Linhas com erro aparecem marcadas, como uma variável escrita errado ou um EAN-13 sem 12 dígitos. Em **Número inicial da sequência** você escolhe onde o `{seq}` começa.

Se a etiqueta não tem nenhuma variável, o app avisa que todas as cópias vão sair iguais.

Se a impressora falhar no meio, o lote pausa. **Tentar de novo** continua da linha atual, sem reimprimir as anteriores.

A última lista usada fica salva na etiqueta, para o próximo lote.

## Planilha do Google

A planilha precisa estar compartilhada como "qualquer pessoa com o link". O app não pede login.

A cópia baixada fica salva junto com o link. Sem internet, o app reimprime com essa cópia. Com internet, **Atualizar planilha** busca a versão atual.

Essa é a única função do app que usa a internet.

## Exemplo: etiquetas de patrimônio

1. Crie uma etiqueta com o texto "Patrimônio {seq:4}" e um código de barras Code 128 com `PAT{seq:4}`.
2. Em **Imprimir em lote**, cole uma lista com 20 linhas, uma para cada equipamento, com o nome dele.
3. Use `{col1}` num segundo texto para imprimir o nome do equipamento.
4. Confira a revisão e imprima. Saem 20 etiquetas, de PAT0001 a PAT0020.
