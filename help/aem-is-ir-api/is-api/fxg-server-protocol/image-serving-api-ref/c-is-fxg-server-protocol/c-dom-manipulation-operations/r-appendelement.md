---
title: appendElement
description: Hängen Sie XML an eine s7 elementID an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# appendElement{#appendelement}

Anhängen von XML an ein s7:elementID.

`appendElement.elementID=<XML>`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, wird der `<XML>` als untergeordnetes Element angehängt. Die `<XML>` muss kodiert sein.

## Beispiel {#section-4368570aa198485d91b73b4d0741478f}

Angenommen, für einen Gruppenknoten ist ein `s7:elementID="group1"` definiert, dann ist Folgendes gültig:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel wird eine untergeordnete Textgrafik an `group1` angehängt.
