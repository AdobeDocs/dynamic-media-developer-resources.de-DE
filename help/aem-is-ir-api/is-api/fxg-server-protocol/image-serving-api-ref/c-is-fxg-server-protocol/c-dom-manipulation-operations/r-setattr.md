---
title: setAttr
description: Legen Sie ein beliebiges Attribut für eine bestimmte s7-Element-ID fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: 'https://experienceleague.adobe.com/0O1uOLXsh-5PkBnXugpQYJHDAZep49WO3AA4hjClODk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 1%

---

# setAttr{#setattr}

Legen Sie ein beliebiges Attribut für ein bestimmtes s7:elementID fest.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, können Sie die Attribute für diesen Knoten bearbeiten. Sie können beliebig viele Attribut-Wert-Paare festlegen. Die Attribute müssen nicht bereits in der FXG definiert sein, sie müssen jedoch für das Knotenelement gültig sein. Alle Werte zwischen `{}` müssen mit Escape-Zeichen versehen werden.

## Beispiel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Angenommen, für einen `BitmapGraphic` Knoten ist ein `s7:elementID="Group1"` definiert, dann ist Folgendes gültig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In diesem Beispiel werden *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* und *[!DNL scaleY]* für die `BitmapGraphic` festgelegt und vorhandene Werte überschrieben.
