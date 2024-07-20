---
title: hei
description: Ansichthöhe. Gibt die Höhe des Antwortbilds (Ansichtsbild) an, wenn die Anpassung in der Anforderung nicht vorhanden ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

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

Wenn sowohl `wid=` als auch `scl=` angegeben sind, kann das zusammengesetzte Bild gemäß dem Attribut `align=` zugeschnitten werden. Wenn `fit=` vorhanden ist, gibt `hei=` die genaue, minimale oder maximale Höhe des Antwortbilds an. Weitere Informationen finden Sie in der Beschreibung von [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) .

Wenn `scl=` nicht angegeben ist, wird das Composite-Bild skaliert, um passend zu sein. Wenn sowohl `wid=` als auch `hei=` angegeben sind und `scl=` nicht angegeben ist, wird das Bild so skaliert, dass es vollständig in das Breite/Höhe-Rechteck passt, wobei so wenig Hintergrundbereich wie möglich verfügbar gemacht wird. In diesem Fall wird das Bild im Ansichtsrechteck gemäß dem Attribut `align=` positioniert. Der Hintergrundbereich wird mit `bgc=` oder, falls nicht mit `attribute::BkgColor` angegeben, mit  gefüllt.

>[!NOTE]
>
>Wenn die berechnete Größe des Antwortbilds größer als `attribute::MaxPix` ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-534923644a1e464496eeba83dedcbd3c}

Attribut anzeigen. Sie gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-76544d34806d4124a8b173e229cba71f}

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind, hat das Antwortbild entweder die Größe des zusammengesetzten Bildes oder `attribute::DefaultPix`, je nachdem, welcher Wert kleiner ist.

## Beispiele {#section-eb10df7cd67e4733984810aaffd0b9e2}

Fordern Sie ein Bild an, damit es in ein 200 x 200-Rechteck passt. Richten Sie es oben links aus, wenn es nicht quadratisch ist. Jeder Hintergrundbereich wird mit `attribute::BkgColor` gefüllt.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Das gleiche Bild, das mit einer festen Höhe von 200 Pixel bereitgestellt wird, jedoch mit einer variablen Breite, die dem Seitenverhältnis des Bildes entspricht. In diesem Fall hat das zurückgegebene Bild nie Hintergrundfüllbereiche. Und in diesem Fall hätte `align=` überhaupt keine Auswirkung.

`http://server/myRootId/myImageId?hei=200`

## Verwandte Themen {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
