---
description: Stellen Sie XML auf eine s7 elementID ein.
seo-description: Stellen Sie XML auf eine s7 elementID ein.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

Stellen Sie XML auf eine s7:elementID ein.

`setElement.elementID=<XML>`

Wenn ein FXG-Knotenelement eine `s7:elementID` definierte Eigenschaft hat, wird der `<XML>` Wert als untergeordnetes Element ersetzt. The `<XML>` must be encoded.

## Beispiel {#section-f23a998b18994dd3b5d4e1965718db9f}

Wenn ein `s7:elementID="group2"` Attribut für eine `Group` Node definiert ist, ist Folgendes gültig:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel werden alle untergeordneten Elemente aus dem `group2`Knoten entfernt und durch den neuen `TextGraphic` untergeordneten Knoten ersetzt.
