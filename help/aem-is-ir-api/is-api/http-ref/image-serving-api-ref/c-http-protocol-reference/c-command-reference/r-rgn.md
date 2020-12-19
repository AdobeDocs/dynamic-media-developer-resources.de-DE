---
description: Region von Interesse. Gibt einen rechteckigen Interessenbereich (ROI) im Gesamtbild in Pixel an.
seo-description: Region von Interesse. Gibt einen rechteckigen Interessenbereich (ROI) im Gesamtbild in Pixel an.
seo-title: rgn
solution: Experience Manager
title: rgn
topic: Scene7 Image Serving - Image Rendering API
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 3%

---


# rgn{#rgn}

Region von Interesse. Gibt einen rechteckigen Interessenbereich (ROI) im Gesamtbild in Pixel an.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kohle</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke des Composite-Bildes nach oben links des ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Größe</span> </p></td> 
  <td class="stentry"> <p>Größe des ROI in Pixel (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` definiert nur einen ROI, ohne das Bild zu beschneiden. Wenn auch `wid=` und/oder `hei=` größer als die Größe angewendet wird, können zusätzliche Daten aus dem zusammengesetzten Bild im endgültigen Antwortbild sichtbar sein.

## Eigenschaften {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Ansicht. Gilt unabhängig von der aktuellen Ebeneneinstellung.

Alle Bereiche des ROI, die sich außerhalb des Composite-Bildes befinden, werden mit `bgc=` aufgefüllt.

`rgn=` wird vor der endgültigen Skalierung angewendet und mit  `scl=`,  `wid=`,  `hei=`,  `fit=`,  `rect=`oder  `align=`.

## Standard {#section-6a3df8f670084def900ffef9dab7e94a}

Gesamtes Composite-Bild ( `rgn=0,0,width,height`).

## Verwandte Themen {#section-07883760f25c4d17aedbee36b7883891}

[cut=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [, align=,fit=,rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
