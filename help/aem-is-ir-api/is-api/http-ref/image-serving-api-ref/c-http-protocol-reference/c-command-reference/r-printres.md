---
description: Druckauflösung. Überschreibt den Wert für die Druckauflösung, der im Antwortbild eingebettet ist.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# printRes{#printres}

Druckauflösung. Überschreibt den Wert für die Druckauflösung, der im Antwortbild eingebettet ist.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Druckauflösung (dpi). </p></td> 
 </tr> 
</table>

Die Druckauflösung wird normalerweise durch `catalog::PrintResolution` bei Katalogeinträgen definiert, andernfalls durch den im Quellbild eingebetteten Wert für die Druckauflösung. Bei einer Vorlage oder einem Verbundbild mit Ebenen ist die in die Antwortdatei eingebettete Standarddruckauflösung die Druckauflösung des Ebenenbilds mit der niedrigsten Ebenenzahl.

Durch Festlegen der Druckauflösung wird die Pixelgröße des Antwortbilds nicht geändert.

## Eigenschaften {#section-03c7910ebe234804a319e5d0d8ef3a74}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` oder die im Quellbild eingebettete Druckauflösung.

## Verwandte Themen {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[Katalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
