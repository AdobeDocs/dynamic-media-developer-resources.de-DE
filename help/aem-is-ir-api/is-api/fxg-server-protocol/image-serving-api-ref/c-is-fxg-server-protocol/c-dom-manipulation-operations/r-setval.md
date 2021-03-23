---
description: Legen Sie einen Textknotenwert für s7 elementID fest.
seo-description: Legen Sie einen Textknotenwert für s7 elementID fest.
seo-title: setVal
solution: Experience Manager
title: setVal
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
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
