---
title: op_growthMask
description: Bild erweitern/erodieren Wendet eine morphologische Dilatation (Radius > 0) oder Erosion (Radius < 0) auf die Maskendaten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
TQID: 'https://experienceleague.adobe.com/-MDsQlyw5ts3RL59hw4-EeF146qdxZqc3fOfzL8BUOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 2%

---

# op_growthMask{#op-growmask}

Bild erweitern/erodieren Wendet eine morphologische Dilatation (Radius > 0) oder Erosion (Radius &lt; 0) auf die Maskendaten an.

`op_growMask= *`Radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Radius</span> </p> </td> 
  <td class="stentry"> <p>Der Radius wird in Pixeln erweitert/erodiert, wobei davon ausgegangen wird, dass der Radius für die Maske mit voller Auflösung gilt, und daher für Masken mit niedrigerer Auflösung herunterskaliert wird (int -100..100). </p></td> 
 </tr> 
</table>

Wird hauptsächlich verwendet, um eine Maske leicht zu vergrößern oder zu verkleinern, um Artefakte am Rand der Maske zu vermeiden.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gilt für die aktuelle Ebene oder, falls `layer=comp`, für Ebene `0`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, für keine Veränderung.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
