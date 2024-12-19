---
description: Typ der Miniaturansicht. Beschreibt, wie eine Miniaturansicht für dieses Bild generiert wird.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# ThumbType{#thumbtype}

Typ der Miniaturansicht. Beschreibt, wie eine Miniaturansicht für dieses Bild generiert wird.

Die folgenden Typen von Miniaturansichten werden unterstützt:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Zuschneiden (1) </p></td> 
  <td class="stentry"> <p>Beschneiden Sie das Bild auf das Seitenverhältnis der Miniatur. Sofern das Seitenverhältnis von Miniaturbild und Bild nicht genau identisch sind, wird ein Teil des Bildes abgeschnitten, um sicherzustellen, dass das gesamte Miniaturbild mit Bilddaten gefüllt ist. Das Rechteck für den Zuschnitt wird im Bild mithilfe <span class="codeph"> Attributs positioniert::ThumbHorizAlign</span> und <span class="codeph"> Attributs::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Anpassen (2) </p></td> 
  <td class="stentry"> <p>Passt das gesamte Bild in das Rechteck der Miniatur an. Das Bild wird mithilfe <span class="codeph"> Attributs::ThumbHorizAlign</span> und <span class="codeph"> Attributs::ThumbVertAlign</span> innerhalb des Rechtecks der Miniatur positioniert, und jeder zusätzliche Platz wird mit <span class="codeph"> Attribut::ThumbBkgColor</span> gefüllt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textur (3) </p></td> 
  <td class="stentry"> <p>Beschneiden Sie das Bild auf Grundlage der Auflösung. Das Bild wird nach dem Verhältnis <span class="codeph"> Katalog::ThumbRes</span> zu <span class="codeph"> Katalog::Resolution</span> skaliert. Wenn das resultierende Bild größer als die Miniaturansicht ist, wird es abgeschnitten und an die Größe angepasst. Wenn das skalierte Bild kleiner als die Miniaturansicht ist, wird der verbleibende Bereich mit <span class="codeph"> Attribut gefüllt::ThumbBkgColor</span>. <span class="codeph">::ThumbHorizAlign</span> und <span class="codeph">::ThumbVertAlign</span> werden verwendet, um die Position des Zuschnittsrechtecks in einem größeren Bild oder die Position eines kleineren Bildes in der Miniatur zu bestimmen. </p></td> 
 </tr> 
</table>

Clients fordern Bildminiaturansichten mit `req=tmb` an.

## Eigenschaften {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Aufzählungswert. Gültige Werte sind 1, 2 oder 3, die den Typen „Zuschneiden“, „Anpassen“ und „Textur“ entsprechen.

## Standard {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` wird verwendet, wenn das Feld nicht vorhanden ist, der Wert 0 ist oder das Feld leer ist.

## Verwandte Themen {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69), [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Miniaturskalierung](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
