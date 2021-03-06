---
description: Druckauflösung. Überschreibt den Wert der Druckauflösung, der im Antwortbild eingebettet ist.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# printRes{#printres}

Druckauflösung. Überschreibt den Wert der Druckauflösung, der im Antwortbild eingebettet ist.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Druckauflösung (dpi). </p></td> 
 </tr> 
</table>

Die Druckauflösung wird normalerweise von `catalog::PrintResolution` im Fall eines Katalogeintrags definiert, andernfalls vom Wert der Druckauflösung, der in das Quellbild eingebettet ist. Bei einer Vorlage oder einem Bild mit mehreren Ebenen ist die in die Antwortdatei eingebettete Standarddruckauflösung die Druckauflösung des Ebenenbilds mit der niedrigsten Ebenennummer.

Durch das Festlegen der Druckauflösung wird die Pixelgröße des Antwortbilds nicht geändert.

## Eigenschaften {#section-03c7910ebe234804a319e5d0d8ef3a74}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` oder die im Quellbild eingebettete Druckauflösung.

## Verwandte Themen {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
