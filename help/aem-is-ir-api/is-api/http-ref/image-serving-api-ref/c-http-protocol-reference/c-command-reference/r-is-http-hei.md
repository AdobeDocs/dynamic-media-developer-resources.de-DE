---
title: hei
description: Ansichthöhe. Gibt die Höhe des Antwortbilds (Ansichtsbild) an, wenn die Anpassung in der Anforderung nicht vorhanden ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# hei{#hei}

Ansichthöhe. Gibt die Höhe des Antwortbilds (Ansichtsbild) an, wenn die Anpassung in der Anforderung nicht vorhanden ist.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Bildhöhe in Pixel (int größer als 0). </p> </td> 
 </tr> 
</table>

Wenn `wid=` und `scl=` festgelegt sind, kann das zusammengesetzte Bild je nach `align=`-Attribut. Wann `fit=` vorhanden ist, `hei=` gibt die genaue, minimale oder maximale Bildhöhe der Antwort an; siehe Beschreibung von [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) für Details.

Wenn `scl=` nicht angegeben ist, wird das zusammengesetzte Bild auf die Anpassung skaliert. Wenn `wid=` und `hei=` festgelegt sind und `scl=` nicht angegeben ist, wird das Bild so skaliert, dass es vollständig in das Breite/Höhe-Rechteck passt, wobei so wenig Hintergrundbereich wie möglich verfügbar ist. In diesem Fall wird das Bild innerhalb des Ansichtsrechtecks entsprechend der `align=` -Attribut. Der Hintergrundbereich ist mit `bgc=`oder, falls nicht angegeben mit `attribute::BkgColor`.

>[!NOTE]
>
>Ein Fehler wird zurückgegeben, wenn die berechnete Größe des Antwortbilds größer ist als `attribute::MaxPix`.

## Eigenschaften {#section-534923644a1e464496eeba83dedcbd3c}

Attribut anzeigen. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-76544d34806d4124a8b173e229cba71f}

Wenn `wid=`, `hei=`, noch `scl=` angegeben sind, hat das Antwortbild entweder die Größe des zusammengesetzten Bildes oder `attribute::DefaultPix`, je nachdem, welcher Wert kleiner ist.

## Beispiele {#section-eb10df7cd67e4733984810aaffd0b9e2}

Fordern Sie ein Bild an, das in ein 200 x 200-Rechteck passt. Richten Sie es oben links aus, wenn es nicht quadratisch ist. Jeder Hintergrundbereich wird mit `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Das gleiche Bild, das mit einer festen Höhe von 200 Pixel bereitgestellt wird, jedoch mit einer variablen Breite, die dem Seitenverhältnis des Bildes entspricht. In diesem Fall hat das zurückgegebene Bild nie Hintergrundfüllbereiche. Beachten Sie, dass in diesem Fall `align=` keine Wirkung hätte.

`http://server/myRootId/myImageId?hei=200`

## Verwandte Themen {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
