---
description: Legen Sie einen Textknotenwert für s7 elementID fest.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

Legen Sie den Textknotenwert für s7:elementID fest.

`setVal.elementID= *[!DNL value]*`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, kann der Textwert für diesen Knoten bearbeitet werden.

## Beispiel {#section-f574fd66dedd4a219aa537d7bdabea23}

Wenn ein `s7:elementID="paragraph1"`-Attribut für einen `TextGraphic`-Knoten definiert ist, ist Folgendes gültig:

`&setVal.paragraph=Hello`

In diesem Beispiel wird der Textwert für den Absatzknoten auf &quot;Hello&quot;gesetzt.
