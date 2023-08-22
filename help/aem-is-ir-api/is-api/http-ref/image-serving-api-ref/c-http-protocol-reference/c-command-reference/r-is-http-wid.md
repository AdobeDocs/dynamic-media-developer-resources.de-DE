---
title: wid
description: Anzeigebreite. Gibt die Breite des Antwortbilds (Ansichtsbild) an, wenn fit= in der Anforderung nicht vorhanden ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# wid{#wid}

Anzeigebreite. Gibt die Breite des Antwortbilds (Ansichtsbild) an, wenn fit= in der Anforderung nicht vorhanden ist.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0). </p> </td> 
 </tr> 
</table>

Wenn `hei=` und `scl=` festgelegt sind, kann das zusammengesetzte Bild je nach `align=` -Attribut. Wann `fit=` vorhanden ist, `wid=` gibt die genaue, minimale oder maximale Bildbreite der Antwort an; siehe Beschreibung von `fit=` für Details.

Wenn `scl=` nicht angegeben ist, wird das zusammengesetzte Bild auf die Anpassung skaliert. Wenn `wid=` und `hei=` festgelegt sind und `scl=` nicht angegeben ist, wird das Bild so skaliert, dass es vollständig in das Breite/Höhe-Rechteck passt, wobei so wenig Hintergrundbereich wie möglich verfügbar ist. In diesem Fall wird das Bild innerhalb des Ansichtsrechtecks entsprechend der `align=` -Attribut.

>[!NOTE]
>
>Ein Fehler wird zurückgegeben, wenn die berechnete oder die standardmäßige Antwortbildgröße größer ist als `attribute::MaxPix`.

## Standard {#section-976d4c8554a34c899f85d172f6ac6f58}

Wenn `wid=`, `hei=`, noch `scl=` angegeben sind, hat das Antwortbild entweder die Größe des zusammengesetzten Bildes oder `attribute::DefaultPix`, je nachdem, welcher Wert kleiner ist.

## Eigenschaften {#section-c93b7ce1b0d2475f80b06264b45d1285}

Attribut anzeigen. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Beispiel {#section-82bc98b7c15a451bbe9b915d414c0470}

Fordern Sie ein Bild an, das in ein 200 x 200-Rechteck passt. Richten Sie es oben rechts aus, wenn es nicht quadratisch ist. Jeder Hintergrundbereich wird mit `attribute::BkgColor`.

` http:// *`Server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Das gleiche Bild, das mit einer festen Breite von 200 Pixel bereitgestellt wird, jedoch mit einer variablen Höhe, um das Seitenverhältnis des Bildes beizubehalten. In diesem Fall hat das zurückgegebene Bild nie Hintergrundfüllbereiche. Beachten Sie, dass in diesem Fall align= überhaupt keine Wirkung hätte.

` http:// *`Server`*/myRootId/myImageId?wid=200`

## Verwandte Themen {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
