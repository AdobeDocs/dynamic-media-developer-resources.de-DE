---
description: Stellen Sie XML auf eine s7 elementID ein.
seo-description: Stellen Sie XML auf eine s7 elementID ein.
seo-title: setElement
solution: Experience Manager
title: setElement
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# setElement{#setelement}

Stellen Sie XML auf eine s7:elementID ein.

`setElement.elementID=<XML>`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, wird der `<XML>`-Wert als untergeordnetes Element ersetzt. Das `<XML>` muss kodiert sein.

## Beispiel {#section-f23a998b18994dd3b5d4e1965718db9f}

Wenn ein `s7:elementID="group2"`-Attribut für einen `Group`-Knoten definiert ist, ist Folgendes gültig:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel werden alle untergeordneten Elemente aus dem Knoten `group2`entfernt und durch den neuen untergeordneten Knoten `TextGraphic` ersetzt.
