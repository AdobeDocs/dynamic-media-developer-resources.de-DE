---
description: Hängen Sie XML an eine s7 elementID an.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# appendElement{#appendelement}

Hängen Sie XML an eine s7:elementID an.

`appendElement.elementID=<XML>`

Wenn für ein FXG-Knotenelement `s7:elementID` definiert ist, wird der Wert `<XML>` als untergeordnetes Element angehängt. `<XML>` muss kodiert sein.

## Beispiel {#section-4368570aa198485d91b73b4d0741478f}

Angenommen, ein `s7:elementID="group1"` -Attribut ist für einen Gruppenknoten definiert, dann ist Folgendes gültig:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel wird ein untergeordnetes Textgrafik-Element an `group1` angehängt.
