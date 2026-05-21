---
title: op_growth
description: Bild erweitern/erodieren Wendet eine morphologische Erweiterung (Radius > 0) oder Erosion (Radius < 0) auf die Bilddaten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
TQID: 'https://experienceleague.adobe.com/vNFqqzcSqktgB5ohUZjqf0RtQNOD-t7fxITR2gZl-T4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# op_growth{#op-grow}

Bild erweitern/erodieren Wendet eine morphologische Erweiterung (Radius > 0) oder Erosion (Radius &lt; 0) auf die Bilddaten an.

`op_grow= *`Radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Radius</span></span> </p> </td> 
  <td class="stentry"> <p>Dilat/Erodierradius in Pixeln (int -100..100). </p></td> 
 </tr> 
</table>

`*`Radius`*` wird in Pixeln relativ zum zusammengesetzten Bild angegeben. Wenn das Bild farbig ist, wird jede Komponente unabhängig verarbeitet.

Wird hauptsächlich zum Ändern der Größe von Ebeneneffekten verwendet. Dies ist auch nützlich, um spezielle Effekte auf Textebenen oder einfarbigen Ebenen mit Masken zu erzielen.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Ebenenattribut. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, für keine Veränderung.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
