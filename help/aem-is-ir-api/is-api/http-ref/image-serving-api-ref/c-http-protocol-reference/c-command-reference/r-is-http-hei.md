---
description: Höhe der Ansicht. Gibt die Höhe des Antwortbilds (Ansicht) an, wenn die Anpassung in der Anforderung nicht vorhanden ist.
seo-description: Höhe der Ansicht. Gibt die Höhe des Antwortbilds (Ansicht) an, wenn die Anpassung in der Anforderung nicht vorhanden ist.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 4%

---


# hei{#hei}

Höhe der Ansicht. Gibt die Höhe des Antwortbilds (Ansicht) an, wenn die Anpassung in der Anforderung nicht vorhanden ist.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Bildhöhe in Pixel (int größer als 0). </p> </td> 
 </tr> 
</table>

Wenn sowohl `wid=` als auch `scl=` angegeben sind, kann das Composite-Bild gemäß dem Attribut `align=`abgeschnitten werden. Wenn `fit=` vorhanden ist, gibt `hei=` die exakte, die minimale oder die maximale Bildhöhe für die Antwort an. Weitere Informationen finden Sie in der Beschreibung von ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`.

Wenn `scl=` nicht angegeben ist, wird das Composite-Bild an die Größe angepasst. Wenn sowohl `wid=` als auch `hei=` angegeben sind und `scl=` nicht angegeben ist, wird das Bild so skaliert, dass es vollständig in das Rechteck &quot;Breite/Höhe&quot;passt, wobei so wenig Hintergrundbereich wie möglich sichtbar bleibt. In diesem Fall wird das Ansicht gemäß dem Attribut `align=` innerhalb des Rechtecks positioniert. Der Hintergrundbereich wird mit `bgc=` oder, falls nicht mit `attribute::BkgColor` angegeben, gefüllt.

>[!NOTE]
>
>Wenn die berechnete Antwortbildgröße größer als `attribute::MaxPix` ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-534923644a1e464496eeba83dedcbd3c}

Ansicht. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-76544d34806d4124a8b173e229cba71f}

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind, hat das Antwortbild entweder die Größe des Composite-Bildes oder `attribute::DefaultPix`, je nachdem, welcher Wert kleiner ist.

## Beispiele {#section-eb10df7cd67e4733984810aaffd0b9e2}

ein Bild anfordern, das in ein Rechteck der Größe 200 x 200 passt; Richten Sie das Bild oben links aus, wenn es nicht quadratisch ist. Jeder Hintergrundbereich wird mit `attribute::BkgColor` gefüllt.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Das gleiche Bild, das mit einer festen Höhe von 200 Pixel, jedoch mit einer variablen Breite geliefert wird, die dem Seitenverhältnis des Bilds entspricht. In diesem Fall hat das zurückgegebene Bild nie Füllbereiche im Hintergrund. Beachten Sie, dass `align=` in diesem Fall keinerlei Auswirkungen haben würde.

`http://server/myRootId/myImageId?hei=200`

## Verwandte Themen {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)  [rgn=attribute::DefaultPix,attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
