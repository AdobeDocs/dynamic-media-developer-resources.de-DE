---
title: op_expandMask
description: Bild verkleinern/erodieren. Wendet eine morphologische Verfärbung (Radius > 0) oder eine Erdung (Radius < 0) auf die Maskendaten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# op_expandMask{#op-growmask}

Bild verkleinern/erodieren. Wendet eine morphologische Verfärbung (Radius > 0) oder eine Erdung (Radius &lt; 0) auf die Maskendaten an.

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Dilate/Erode radius in Pixeln, wobei angenommen wird, dass der Radius auf die Vollauflösungsmaske angewendet wird, und daher für heruntergesampelte Masken herabskaliert wird (int -100..100). </p></td> 
 </tr> 
</table>

Wird hauptsächlich verwendet, um eine Maske geringfügig zu vergrößern oder zu verkleinern, um Artefakte um den Rand der Maske zu vermeiden.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gilt für die aktuelle Ebene oder Ebene `0` if `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, ohne Änderung.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_expand](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_expandMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
