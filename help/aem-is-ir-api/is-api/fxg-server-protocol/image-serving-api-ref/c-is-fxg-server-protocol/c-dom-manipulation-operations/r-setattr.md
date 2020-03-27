---
description: Legen Sie ein beliebiges Attribut für eine angegebene s7 elementID fest.
seo-description: Legen Sie ein beliebiges Attribut für eine angegebene s7 elementID fest.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr{#setattr}

Legen Sie ein beliebiges Attribut für eine gegebene s7:elementID fest.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Wenn ein FXG-Knotenelement eine `s7:elementID` definierte enthält, können Sie die Attribute für diesen Knoten bearbeiten. Sie können beliebig viele Attribut-/Wertpaare einstellen. Die Attribute müssen nicht bereits im FXG definiert sein, sie müssen jedoch für das Knotenelement gültig sein. Alle Werte dazwischen `{}` müssen mit Escapezeichen versehen sein.

## Beispiel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Wenn ein `s7:elementID="Group1"` Attribut für eine `BitmapGraphic` Node definiert ist, ist Folgendes gültig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In diesem Beispiel werden die Werte *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* und *[!DNL scaleY]* für die Werte festgelegt `BitmapGraphic` und alle vorhandenen Werte außer Kraft gesetzt.
