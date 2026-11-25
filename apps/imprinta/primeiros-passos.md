---
layout: guia
app: imprinta
title: Primeiros passos | Imprinta
description: Conecte a Niimbot B1 ao Imprinta e imprima a primeira etiqueta.
permalink: /apps/imprinta/primeiros-passos/
---

# Primeiros passos

Este guia leva você do app recém-instalado até a primeira etiqueta impressa. O exemplo é uma etiqueta de carne moída com validade de 3 meses.

## 1. Ligue a impressora

Coloque um rolo na Niimbot B1 e ligue a impressora. Não pareie a B1 nas configurações de Bluetooth do Android. Ela usa Bluetooth Low Energy, e o Imprinta conecta direto, sem pareamento.

## 2. Encontre a impressora no app

1. Na tela inicial, toque em **Configurações**, na barra de baixo.
2. Em **Modelo da impressora**, deixe **Niimbot B1**.
3. Toque em **Procurar impressora (BLE)**. O Android pede a permissão de dispositivos próximos. Permita.
4. Quando o endereço aparecer, escolha o **Rolo em uso**, por exemplo 50 × 30 mm.
5. Toque em **Testar conexão** e depois em **Salvar**.

Se a busca não achar a impressora, digite o endereço à mão. Ele fica numa etiqueta embaixo da B1, no campo `BT_Mac`.

## 3. Crie um grupo

Volte à tela inicial e toque em **Novo grupo**, no fim da lista. Dê o nome "Congelados" e confirme.

## 4. Cadastre a etiqueta

1. Toque em "Congelados" e depois em **Novo item**.
2. Em **Nome da etiqueta**, escreva "Carne moída".
3. Toque em **+** ao lado de **Foto / Ilustrações** e escolha uma ilustração do tema Carnes, aves e peixes.
4. Em **Elementos da etiqueta**, toque em **+ Adicionar elemento**, escolha **Quantidade** e a unidade Gramas. Deixe o valor em branco para digitar na hora.
5. Adicione um elemento **Data**, relativa, com o rótulo "Validade" e "Hoje + 3 meses".
6. Toque em **Salvar**.

A pré-visualização no topo da tela mostra a etiqueta enquanto você edita. Os detalhes de cada elemento estão em [Montar a etiqueta](../etiquetas/).

## 5. Imprima

Toque em **Ir p/ Impressão**. O app conecta na impressora sozinho e o botão mostra "Conectando…" até a conexão sair.

Digite 500 na quantidade, ajuste **Cópias** e toque em **Imprimir**. As etiquetas saem com a validade calculada a partir de hoje.

Da próxima vez, basta abrir o grupo, tocar na etiqueta e imprimir.

## Próximos passos

Se você imprime várias etiquetas parecidas, crie um [Modelo](../modelos/). Para não perder o catálogo ao trocar de celular, faça um [Backup](../backup/).
