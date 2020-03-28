---
description: Hängen Sie XML an eine s7 elementID an.
seo-description: Hängen Sie XML an eine s7 elementID an.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# appendElement{#appendelement}

Hängen Sie XML an eine s7:elementID an.

`appendElement.elementID=<XML>`

Wenn ein FXG-Knotenelement eine `s7:elementID` Definition hat, wird der `<XML>` Wert als untergeordnetes Element angehängt. The `<XML>` must be encoded.

## Beispiel {#section-4368570aa198485d91b73b4d0741478f}

Angenommen, ein `s7:elementID="group1"` Attribut ist für eine Gruppe-Node definiert, ist Folgendes gültig:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel wird ein untergeordnetes Textdiagramm an `group1`angehängt.
