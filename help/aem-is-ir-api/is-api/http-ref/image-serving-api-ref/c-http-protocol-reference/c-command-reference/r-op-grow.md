---
title: op_expand
description: Bild verkleinern/erodieren. Wendet eine morphologische Verfärbung (Radius > 0) oder eine Erdung (Radius < 0) auf die Bilddaten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---

# op_expand{#op-grow}

Bild verkleinern/erodieren. Wendet eine morphologische Verfärbung (Radius > 0) oder eine Erdung (Radius &lt; 0) auf die Bilddaten an.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Radius zum Verdünnen/Erodieren in Pixel (int -100..100). </p></td> 
 </tr> 
</table>

`*`radius`*` in Pixel relativ zum Composite-Bild angegeben. Wenn das Bild farbig ist, wird jede Komponente unabhängig verarbeitet.

Wird hauptsächlich verwendet, um die Größe von Ebeneneffekten zu ändern. Auch nützlich, um besondere Effekte auf Textebenen oder solide Farbschichten mit Masken zu erzielen.

## Eigenschaften {#section-b1c66d65168d4ea695e8662ea690bd4e}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, ohne Änderung.

## Verwandte Themen {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Ebeneneffekte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
