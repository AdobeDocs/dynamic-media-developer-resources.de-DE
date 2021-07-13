---
description: Setzen Sie XML auf eine s7 elementID.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# setElement{#setelement}

Setzen Sie XML auf eine s7:elementID.

`setElement.elementID=<XML>`

Wenn für ein FXG-Knotenelement `s7:elementID` definiert ist, wird der Wert `<XML>` als untergeordnetes Element ersetzt. `<XML>` muss kodiert sein.

## Beispiel {#section-f23a998b18994dd3b5d4e1965718db9f}

Angenommen, ein `s7:elementID="group2"` -Attribut ist für einen `Group` -Knoten definiert, dann ist Folgendes gültig:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel werden alle untergeordneten Elemente aus dem Knoten `group2`entfernt und durch den neuen untergeordneten Knoten `TextGraphic` ersetzt.
