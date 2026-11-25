---
layout: guia
app: imprinta
title: Imprinta
description: Guia de uso do Imprinta, app Android que imprime etiquetas na Niimbot B1 a partir de um catálogo, com um toque.
permalink: /apps/imprinta/
---

# Imprinta

O Imprinta nasceu na cozinha. Etiquetar potes com nome, data e validade no app oficial da impressora exige montar a etiqueta toda vez. O Imprinta inverte isso: você cadastra cada etiqueta uma vez e depois só toca para imprimir. A data do dia, a validade e as quantidades saem calculadas na hora.

O app imprime na Niimbot B1 por Bluetooth, sem pareamento. Serve para qualquer etiqueta que se repete: estoque, escritório, loja, oficina, laboratório ou arquivo.

## Como funciona

O app trabalha com três peças. O **grupo** reúne etiquetas parecidas, por exemplo "Congelados" ou "Despensa". A **etiqueta** guarda o nome, uma imagem e a lista de elementos que saem impressos: textos, datas, quantidades e linhas. O **modelo** é uma etiqueta pronta que serve de ponto de partida para outras.

Nada do que muda a cada uso fica salvo na etiqueta. A data, a quantidade e o número de cópias você ajusta na tela de impressão, e a etiqueta impressa reflete o dia em que saiu da impressora.

## Para que serve

| Uso | Como montar |
|---|---|
| Validade de alimentos | Data "hoje" como "Guardado em" e data "hoje + 3 meses" como "Validade" |
| Porções congeladas | Elemento de quantidade em gramas, digitada na hora de imprimir |
| Organizar a despensa | Nome grande e ilustração do produto |
| Estoque e patrimônio | Código de barras com `{seq}` e impressão em lote a partir de uma planilha |
| Etiqueta com link | QR code no lugar da imagem |
| Pasta de arquivo ou caixa de mudança | Texto livre e data fixa |

## Recursos

| Recurso | O que faz |
|---|---|
| Catálogo | Etiquetas organizadas em grupos, com busca por nome |
| Elementos | Textos, datas fixas ou relativas, quantidades e linhas, cada um com tamanho, fonte e alinhamento |
| Imagens | 210 ilustrações em 19 temas, ou uma foto sua convertida para preto e branco |
| QR code e código de barras | QR code com texto ou link, código de barras Code 128 ou EAN-13 |
| Modelos | Etiquetas prontas com campos para preencher a cada uso |
| Variáveis | Data, hora e numeração dentro do texto, do QR code e do código de barras |
| Impressão em lote | Uma etiqueta por linha de uma lista, de um CSV ou de uma planilha do Google |
| Backup e planilha | Exporta o catálogo num `.zip` e edita os itens numa planilha CSV |

O app tem 22 fontes, interface em português e inglês, e funciona a partir do Android 8.0.

## Impressoras

Hoje o Imprinta imprime na **Niimbot B1**, testada em hardware real. Os rolos aceitos são 50 × 30, 40 × 40, 50 × 50 e 40 × 70 mm. A etiqueta se arranja sozinha pela proporção do rolo. O rolo 50 × 30 mm é o mais testado.

Outros modelos da Niimbot ainda não aparecem na lista, porque não foram testados.

## Versão gratuita e versão Premium

A versão gratuita guarda até 5 etiquetas. Os modelos não entram nessa conta.

A versão Premium libera etiquetas sem limite. É uma compra única pela Google Play, sem assinatura. Comprar a Premium é a forma de contribuir com o desenvolvimento do app.

## Guias

Comece pelos [Primeiros passos](primeiros-passos/). Depois, use os guias conforme a necessidade.

- [Primeiros passos](primeiros-passos/): da impressora ligada à primeira etiqueta impressa.
- [Montar a etiqueta](etiquetas/): elementos, imagem, QR code e código de barras.
- [Imprimir](impressao/): data, quantidades, cópias e erros de conexão.
- [Modelos](modelos/): etiquetas prontas para reaproveitar.
- [Variáveis e lote](lote/): numeração, datas no texto e várias etiquetas de uma vez.
- [Backup e planilha](backup/): levar o catálogo para outro celular e editar itens no Excel.
- [Privacidade](privacidade/): o que o app faz com os seus dados.

## Privacidade em uma frase

O Imprinta não tem servidor, conta, telemetria nem propaganda. O catálogo fica no seu celular, e o app só usa a internet para baixar uma planilha do Google que você mesmo colar.
