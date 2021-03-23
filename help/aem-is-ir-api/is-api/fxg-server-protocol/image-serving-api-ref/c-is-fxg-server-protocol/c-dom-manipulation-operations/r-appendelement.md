---
description: Hängen Sie XML an eine s7 elementID an.
seo-description: Hängen Sie XML an eine s7 elementID an.
seo-title: appendElement
solution: Experience Manager
title: appendElement
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---


# appendElement{#appendelement}

Hängen Sie XML an eine s7:elementID an.

`appendElement.elementID=<XML>`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, wird der `<XML>`-Wert als untergeordnetes Element angehängt. Das `<XML>` muss kodiert sein.

## Beispiel {#section-4368570aa198485d91b73b4d0741478f}

Angenommen, ein `s7:elementID="group1"`-Attribut ist für einen Gruppenknoten definiert, ist Folgendes gültig:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel wird ein untergeordnetes Textdiagramm an `group1` angehängt.
