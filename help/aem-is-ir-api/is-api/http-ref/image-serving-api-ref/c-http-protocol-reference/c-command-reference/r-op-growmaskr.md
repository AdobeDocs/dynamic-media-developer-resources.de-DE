---
description: Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius < 0) auf die Maskendaten an.
seo-description: Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius < 0) auf die Maskendaten an.
seo-title: op_largeMaskR
solution: Experience Manager
title: op_largeMaskR
topic: Scene7 Image Serving - Image Rendering API
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# op_GrowthMaskR{#op-growmaskr}

Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius &lt; 0) auf die Maskendaten an.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixel, wobei <span class="codeph"><span class="varname"> radiusR</span></span> wie vorhanden angewendet wird, unabhängig davon, ob die Maske neu berechnet wird (int -100..100). </p></td> 
 </tr> 
</table>

Wird hauptsächlich dazu verwendet, eine Maske leicht zu vergrößern oder zu verkleinern, um Artefakte um den Rand der Maske zu vermeiden.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gilt für die aktuelle Ebene oder für die Ebene `0`, wenn `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, ohne dass sich dies ändert.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_large](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_largeMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
