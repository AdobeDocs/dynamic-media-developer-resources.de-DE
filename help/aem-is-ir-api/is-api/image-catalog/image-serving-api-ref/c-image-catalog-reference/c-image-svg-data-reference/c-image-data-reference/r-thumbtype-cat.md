---
description: Typ der Miniaturansicht. Beschreibt, wie eine Miniaturansicht für dieses Bild generiert werden soll.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# ThumbType{#thumbtype}

Typ der Miniaturansicht. Beschreibt, wie eine Miniaturansicht für dieses Bild generiert werden soll.

Die folgenden Miniaturansichten werden unterstützt:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Zuschneiden (1) </p></td> 
  <td class="stentry"> <p>Beschneiden Sie das Bild auf das Seitenverhältnis der Miniaturansicht. Sofern das Seitenverhältnis des Rechtecks für Miniaturansichten und des Bildes nicht genau identisch sind, wird ein Teil des Bildes beschnitten, um sicherzustellen, dass das gesamte Rechteck für Miniaturansichten mit Bilddaten gefüllt ist. Das Zuschnittrechteck wird im Bild mithilfe des Attributs <span class="codeph">::ThumbHorizAlign</span> und des Attributs <span class="codeph">::ThumbVertAlign</span> positioniert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Fit (2) </p></td> 
  <td class="stentry"> <p>Passt das gesamte Bild in das Rechteck der Miniaturansicht ein. Das Bild wird innerhalb des Rechtecks der Miniaturansicht mithilfe des Attributs <span class="codeph">::ThumbHorizAlign</span> und des Attributs <span class="codeph">::ThumbVertAlign</span> positioniert und jeder zusätzliche Platz wird mit dem Attribut <span class="codeph"> gefüllt::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textur (3) </p></td> 
  <td class="stentry"> <p>Beschneiden Sie das Bild auf der Grundlage der Auflösung. Das Bild wird im Verhältnis von <span class="codeph"> Katalog::ThumbRes</span> zu <span class="codeph"> Katalog::Resolution</span> skaliert. Wenn das resultierende Bild größer als die Miniaturansicht ist, wird es entsprechend beschnitten. Wenn das skalierte Bild kleiner als die Miniaturansicht ist, wird der verbleibende Bereich mit dem Attribut <span class="codeph"> gefüllt::ThumbBkgColor</span>. <span class="codeph"> attribute::</span> ThumbHorizAlignand- <span class="codeph"> Attribut::</span> ThumbVertAlignare wird verwendet, um die Position des Zuschnittrechtecks innerhalb eines größeren Bildes oder einer Position eines kleineren Bildes innerhalb der Miniaturansicht zu bestimmen. </p></td> 
 </tr> 
</table>

Clients fordern Miniaturansichten mit `req=tmb` -Anforderungen an.

## Eigenschaften {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Enum-Wert. Gültige Werte sind 1, 2 oder 3, was jeweils den Typen Zuschneiden, Anpassen und Textur entspricht.

## Standard {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert 0 ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f),  [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69),  [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [ Skalierung der Miniaturansichten](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
