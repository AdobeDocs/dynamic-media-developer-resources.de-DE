---
title: setVal
description: Legen Sie den Textknotenwert für s7 elementID fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---

# setVal{#setval}

Legen Sie den Wert des Textknotens für s7:elementID fest.

`setVal.elementID= *[!DNL value]*`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, kann der Textwert für diesen Knoten bearbeitet werden.

## Beispiel {#section-f574fd66dedd4a219aa537d7bdabea23}

Angenommen, für einen `TextGraphic` Knoten ist ein `s7:elementID="paragraph1"` definiert, dann ist Folgendes gültig:

`&setVal.paragraph=Hello`

In diesem Beispiel wird der Textwert für den Absatzknoten auf „Hallo“ festgelegt.
