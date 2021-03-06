---
description: Legen Sie ein beliebiges Attribut für eine gegebene s7 elementID fest.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

Legen Sie ein beliebiges Attribut für eine gegebene s7:elementID fest.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, können Sie die Attribute für diesen Knoten bearbeiten. Sie können beliebig viele Attribut-/Wertpaare festlegen. Die Attribute müssen nicht bereits im FXG definiert sein, sie müssen jedoch für das Knotenelement gültig sein. Alle Werte zwischen `{}` müssen maskiert werden.

## Beispiel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Angenommen, ein `s7:elementID="Group1"`-Attribut ist für einen `BitmapGraphic`-Knoten definiert, dann ist Folgendes gültig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In diesem Beispiel werden die *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* und *[!DNL scaleY]* für `BitmapGraphic` festgelegt und vorhandene Werte werden überschrieben.
