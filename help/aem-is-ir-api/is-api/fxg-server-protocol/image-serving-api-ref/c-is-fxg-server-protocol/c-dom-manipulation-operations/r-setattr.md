---
description: Legen Sie ein beliebiges Attribut für eine angegebene s7 elementID fest.
seo-description: Legen Sie ein beliebiges Attribut für eine angegebene s7 elementID fest.
seo-title: setAttr
solution: Experience Manager
title: setAttr
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# setAttr{#setattr}

Legen Sie ein beliebiges Attribut für eine gegebene s7:elementID fest.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, können Sie die Attribute für diesen Knoten bearbeiten. Sie können beliebig viele Attribut-/Wertpaare einstellen. Die Attribute müssen nicht bereits im FXG definiert sein, sie müssen jedoch für das Knotenelement gültig sein. Alle Werte zwischen `{}` müssen Escapezeichen sein.

## Beispiel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Angenommen, ein `s7:elementID="Group1"`-Attribut ist für einen `BitmapGraphic`-Knoten definiert, dann ist Folgendes gültig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In diesem Beispiel werden die Werte *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* und *[!DNL scaleY]* für `BitmapGraphic` festgelegt und alle vorhandenen Werte außer Kraft gesetzt.
