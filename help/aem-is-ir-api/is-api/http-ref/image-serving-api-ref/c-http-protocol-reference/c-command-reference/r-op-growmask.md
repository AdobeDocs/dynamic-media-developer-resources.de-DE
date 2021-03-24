---
description: Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius < 0) auf die Maskendaten an.
solution: Experience Manager
title: op_largeMask
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# op_GrowthMask{#op-growmask}

Bild vervielfältigen/erodieren. Wendet einen morphologischen Farbverlauf (Radius > 0) oder eine Erosion (Radius &lt; 0) auf die Maskendaten an.

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixeln, wobei angenommen wird, dass der Radius auf die Maske mit voller Auflösung angewendet wird und daher für neu berechnete Masken verringert wird (int -100..100). </p></td> 
 </tr> 
</table>

Wird hauptsächlich dazu verwendet, eine Maske leicht zu vergrößern oder zu verkleinern, um Artefakte um den Rand der Maske zu vermeiden.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gilt für die aktuelle Ebene oder für die Ebene `0`, wenn `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, ohne dass sich dies ändert.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_large](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_largeMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
