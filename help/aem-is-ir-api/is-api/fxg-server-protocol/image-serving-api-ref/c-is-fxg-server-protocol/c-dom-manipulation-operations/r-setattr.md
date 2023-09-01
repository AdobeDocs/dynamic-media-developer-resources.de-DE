---
title: setAttr
description: Legen Sie ein beliebiges Attribut für eine gegebene s7 elementID fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

Legen Sie ein beliebiges Attribut für eine gegebene s7:elementID fest.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Wenn ein FXG-Knotenelement eine `s7:elementID` definiert haben, können Sie die Attribute für diesen Knoten bearbeiten. Sie können beliebig viele Attribut-/Wertpaare festlegen. Die Attribute müssen nicht bereits im FXG definiert sein, sie müssen jedoch für das Knotenelement gültig sein. Alle Werte dazwischen `{}` muss maskiert sein.

## Beispiel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Angenommen, `s7:elementID="Group1"` -Attribut für `BitmapGraphic` -Knoten verwenden, ist Folgendes gültig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In diesem Beispiel wird die *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, und *[!DNL scaleY]* für die `BitmapGraphic` und überschreibt alle vorhandenen Werte.
