---
title: printRes
description: Druckauflösung. Überschreibt den Wert der Druckauflösung, der im Antwortbild eingebettet ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

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

Die Druckauflösung wird normalerweise durch `catalog::PrintResolution` definiert, wenn es sich um einen Katalogeintrag handelt, andernfalls durch den Wert für die Druckauflösung, der in das Quellbild eingebettet ist. Wenn es eine Vorlage oder ein mehrschichtiges Composite-Bild gibt, ist die standardmäßige Druckauflösung, die in die Antwortdatei eingebettet ist, die Druckauflösung des Ebenen-Bildes mit der niedrigsten Ebenennummer.

Durch das Festlegen der Druckauflösung wird die Pixelgröße des Antwortbilds nicht geändert.

## Eigenschaften {#section-03c7910ebe234804a319e5d0d8ef3a74}

Anforderungsattribut. Sie gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
Oder die im Quellbild eingebettete Druckauflösung.

## Verwandte Themen {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
