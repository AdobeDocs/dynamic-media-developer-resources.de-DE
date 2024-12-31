---
title: WID
description: Breite anzeigen. Gibt die Breite des Antwortbildes (Ansichtsbild) an, wenn fit= in der Anfrage nicht vorhanden ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# WID{#wid}

Breite anzeigen. Gibt die Breite des Antwortbildes (Ansichtsbild) an, wenn fit= in der Anfrage nicht vorhanden ist.

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Val </span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0). </p> </td> 
 </tr> 
</table>

Wenn sowohl `hei=` als auch `scl=` angegeben sind, kann das zusammengesetzte Bild gemäß dem `align=`-Attribut abgeschnitten werden. Wenn `fit=` vorhanden ist, gibt `wid=` die genaue, die minimale oder die maximale Breite des Antwortbildes an. Weitere Informationen finden Sie in der Beschreibung von `fit=`.

Wenn `scl=` nicht angegeben ist, wird das zusammengesetzte Bild so skaliert, dass es passt. Wenn sowohl `wid=` als auch `hei=` angegeben sind und `scl=` nicht angegeben ist, wird das Bild so skaliert, dass es vollständig in das wid/hei-Rechteck passt, sodass möglichst wenig Hintergrundbereich belichtet wird. In diesem Fall wird das Bild entsprechend dem `align=`-Attribut innerhalb des Ansichtsrechtecks positioniert.

>[!NOTE]
>
>Ein Fehler wird zurückgegeben, wenn die berechnete oder standardmäßige Größe des Antwortbildes größer als `attribute::MaxPix` ist.

## Standard {#section-976d4c8554a34c899f85d172f6ac6f58}

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind, hat das Antwortbild entweder die Größe des zusammengesetzten Bildes oder `attribute::DefaultPix`, je nachdem, welcher Wert kleiner ist.

## Eigenschaften {#section-c93b7ce1b0d2475f80b06264b45d1285}

Attribut anzeigen. Sie gilt unabhängig von der aktuellen Ebeneneinstellung.

## Beispiel {#section-82bc98b7c15a451bbe9b915d414c0470}

Fordern Sie ein Bild an, damit es in ein Rechteck von 200 x 200 passt. Wenn es nicht quadratisch ist, richten Sie es nach oben rechts aus. Jeder Hintergrundbereich ist mit `attribute::BkgColor` gefüllt.

` http:// *`Server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Gleiches Bild, bereitgestellt mit einer festen Breite von 200 Pixel, aber mit einer variablen Höhe, um das Seitenverhältnis des Bildes beizubehalten. In diesem Fall hat das zurückgegebene Bild keine Hintergrundfüllbereiche. In diesem Fall hätten `align=` keinerlei Wirkung.

` http:// *`Server`*/myRootId/myImageId?wid=200`

## Verwandte Themen {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
