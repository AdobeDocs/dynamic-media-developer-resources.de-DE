---
title: setVal
description: Legen Sie den Textknotenwert für s7 elementID fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# setVal{#setval}

Legen Sie den Textknotenwert für s7:elementID fest.

`setVal.elementID= *[!DNL value]*`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, kann der Textwert für diesen Knoten bearbeitet werden.

## Beispiel {#section-f574fd66dedd4a219aa537d7bdabea23}

Angenommen, für einen `TextGraphic` Knoten ist ein `s7:elementID="paragraph1"` definiert, dann ist Folgendes gültig:

`&setVal.paragraph=Hello`

In diesem Beispiel wird der Textwert für den Absatzknoten auf „Hallo“ festgelegt.
