---
title: rgn
description: Region von Interesse. Gibt einen rechteckigen Bereich von Interesse (ROI) im Composite-Bild an, ausgedrückt in Pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# rgn{#rgn}

Region von Interesse. Gibt einen rechteckigen Bereich von Interesse (ROI) im Composite-Bild an, ausgedrückt in Pixel.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke des Composite-Bildes oben links im ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Größe</span> </p></td> 
  <td class="stentry"> <p>Größe des ROI in Pixel (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` definiert nur einen ROI, ohne das Bild zuzuschneiden. Wann `wid=` und/oder `hei=` größer als die Größe wird auch angewendet, zusätzliche Daten aus dem zusammengesetzten Bild können im endgültigen Antwortbild sichtbar sein.

## Eigenschaften {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Attribut anzeigen. Gilt unabhängig von der aktuellen Ebeneneinstellung.

Alle Bereiche des ROI, die sich außerhalb des Composite-Bilds befinden, werden mit `bgc=`.

`rgn=` vor der endgültigen Skalierung und Anpassung mit `scl=`, `wid=`, `hei=`, `fit=`, `rect=`oder `align=`.

## Standard {#section-6a3df8f670084def900ffef9dab7e94a}

Gesamtes Composite-Bild ( `rgn=0,0,width,height`).

## Verwandte Themen {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [expand=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
