---
description: Legen Sie einen Textknotenwert für s7 elementID fest.
seo-description: Legen Sie einen Textknotenwert für s7 elementID fest.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVal{#setval}

Legen Sie den Textknotenwert für s7:elementID fest.

`setVal.elementID= *[!DNL value]*`

Wenn ein FXG-Knotenelement eine `s7:elementID` definierte enthält, kann der Textwert für diesen Knoten bearbeitet werden.

## Beispiel {#section-f574fd66dedd4a219aa537d7bdabea23}

Wenn ein `s7:elementID="paragraph1"` Attribut für eine `TextGraphic` Node definiert ist, ist Folgendes gültig:

`&setVal.paragraph=Hello`

In diesem Beispiel wird der Textwert für den Absatzknoten auf &quot;Hello&quot;gesetzt.
