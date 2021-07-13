---
description: Bild verkleinern/erodieren. Wendet eine morphologische Verfärbung (Radius > 0) oder eine Erdung (Radius < 0) auf die Maskendaten an.
solution: Experience Manager
title: op_expandMaskR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# op_expandMaskR{#op-growmaskr}

Bild verkleinern/erodieren. Wendet eine morphologische Verfärbung (Radius > 0) oder eine Erdung (Radius &lt; 0) auf die Maskendaten an.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/Erode radius in Pixeln, wobei <span class="codeph"><span class="varname"> radiusR</span></span> wie besehen angewendet wird, unabhängig davon, ob die Maske heruntergesampelt ist (int -100..100). </p></td> 
 </tr> 
</table>

Wird hauptsächlich verwendet, um eine Maske geringfügig zu vergrößern oder zu verkleinern, um Artefakte um den Rand der Maske zu vermeiden.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gilt für die aktuelle Ebene oder für die Ebene `0`, wenn `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, ohne Änderung.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_expand](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_expandMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
