---
description: Breite der Ansicht. Gibt die Breite des Antwortbilds (Ansicht Image) an, wenn fit= in der Anforderung nicht vorhanden ist.
seo-description: Breite der Ansicht. Gibt die Breite des Antwortbilds (Ansicht Image) an, wenn fit= in der Anforderung nicht vorhanden ist.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

Breite der Ansicht. Gibt die Breite des Antwortbilds (Ansicht Image) an, wenn fit= in der Anforderung nicht vorhanden ist.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0). </p> </td> 
 </tr> 
</table>

Wenn sowohl `hei=` als auch `scl=` angegeben sind, kann das Composite-Bild entsprechend dem `align=` Attribut abgeschnitten werden. Wenn `fit=` vorhanden, `wid=` gibt die genaue, die minimale oder die maximale Bildbreite der Antwort an. Einzelheiten finden Sie in der Beschreibung der `fit=` .

Wenn `scl=` kein Wert angegeben ist, wird das Composite-Bild auf die Größe skaliert. Wenn sowohl `wid=` als auch `hei=` angegeben sind und nicht angegeben `scl=` ist, wird das Bild so skaliert, dass es vollständig in das Rechteck &quot;Breite/Höhe&quot;passt, sodass so wenig Hintergrundbereich wie möglich offen bleibt. In diesem Fall wird das Ansicht gemäß dem `align=` Attribut innerhalb des Rechtecks positioniert.

>[!NOTE]
>
>Wenn die berechnete oder standardmäßige Antwortbildgröße größer als `attribute::MaxPix`ist, wird ein Fehler zurückgegeben.

## Standard {#section-976d4c8554a34c899f85d172f6ac6f58}

Wenn weder `wid=`, `hei=`noch `scl=` angegeben, hat das Antwortbild entweder die Größe des Composite-Bildes oder `attribute::DefaultPix`(je nachdem, welcher Wert kleiner ist).

## Eigenschaften {#section-c93b7ce1b0d2475f80b06264b45d1285}

Ansicht. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Beispiel {#section-82bc98b7c15a451bbe9b915d414c0470}

ein Bild anfordern, das in ein Rechteck der Größe 200 x 200 passt; Richten Sie das Bild oben rechts aus, wenn es nicht quadratisch ist. Jeder Hintergrundbereich ist mit `attribute::BkgColor`gefüllt.

` http:// *`Server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Das gleiche Bild, das mit einer festen Breite von 200 Pixeln geliefert wird, jedoch mit einer variablen Höhe, um das Seitenverhältnis des Bilds beizubehalten. In diesem Fall hat das zurückgegebene Bild nie Füllbereiche im Hintergrund. Beachten Sie, dass in diesem Fall &quot;align=&quot;keine Auswirkung haben würde.

` http:// *`Server`*/myRootId/myImageId?wid=200`

## Verwandte Themen {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
