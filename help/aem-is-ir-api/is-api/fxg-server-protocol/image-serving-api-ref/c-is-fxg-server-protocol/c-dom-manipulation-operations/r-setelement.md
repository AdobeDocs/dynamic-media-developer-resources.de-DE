---
title: setElement
description: Setzen Sie XML auf eine s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

Setzen Sie XML auf eine s7:elementID.

`setElement.elementID=<XML>`

Wenn ein FXG-Knotenelement eine `s7:elementID` definiert, wird die `<XML>` -Wert als untergeordnetes Element ersetzt. Die `<XML>` muss kodiert sein.

## Beispiel {#section-f23a998b18994dd3b5d4e1965718db9f}

Angenommen, `s7:elementID="group2"` -Attribut für `Group` -Knoten ist Folgendes gültig:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In diesem Beispiel werden alle untergeordneten Elemente aus dem `group2`Knoten und ersetzt sie durch neue `TextGraphic` untergeordneten Knoten.
