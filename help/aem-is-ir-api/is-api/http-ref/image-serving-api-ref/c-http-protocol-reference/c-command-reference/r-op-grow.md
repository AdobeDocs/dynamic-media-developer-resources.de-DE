---
description: Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius < 0) auf die Bilddaten an.
seo-description: Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius < 0) auf die Bilddaten an.
seo-title: op_large
solution: Experience Manager
title: op_large
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# op_Growth{#op-grow}

Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius &lt; 0) auf die Bilddaten an.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixel (int -100..100). </p></td> 
 </tr> 
</table>

`*``*` Radiusis in Pixeln relativ zum Composite-Bild. Wenn das Bild farbig ist, wird jede Komponente unabhängig verarbeitet.

Wird hauptsächlich zur Änderung der Größe von Ebeneneffekten verwendet. Auch nützlich, um spezielle Effekte auf Textebenen oder Vollfarben-Ebenen mit Masken zu erzielen.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, ohne dass sich dies ändert.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
