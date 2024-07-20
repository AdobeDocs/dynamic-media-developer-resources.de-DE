---
title: Größe
description: Decal size. Breite, Höhe und Dicke eines dekalen Materialobjekts.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---

# Größe{#size}

Decal size. Breite, Höhe und Dicke eines dekalen Materialobjekts.

## Eigenschaften {#section-967bf1112eec4032a91ed0c8a7b10a07}

Drei reale Zahlen, durch Kommas getrennt. Das darf nicht negativ sein. Setzen Sie nicht verwendete Werte auf 0. Nachfolgende Nullen können weggelassen werden.

Geben Sie nur Breite und Höhe an, wenn das Bild so gestreckt werden soll, dass es an die angegebene Größe angepasst wird (das Seitenverhältnis kann sich ändern). Legen Sie entweder Breite oder Höhe fest, um das Bild proportional zu skalieren. Legen Sie sowohl Breite als auch Höhe auf 0 fest, um `catalog::Resolution`zur Bestimmung der Objektgröße zu verwenden.

Geben Sie einen Dickenwert an, um dem Decal-Objekt einen Schlagschatten hinzuzufügen. Optional für dekale Materialien, von allen anderen Materialien ignoriert.

## Standard {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Dies bedeutet, dass die Dekorgröße anhand von catalog::Resolution bestimmt werden soll und dass das Objekt keine Dicke hat (daher wird kein Schlagschatten gerendert).

## Beispiele {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>Der Decal ist auf eine Größe von 12 x 3 Zoll gezwungen und hat keine Dicke (d. h. keinen Schlagschatten). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>Der Abtastraum ist 5 Zoll breit, die Höhe wird durch das Seitenverhältnis des Bildes bestimmt und ein Schlagschatten wird basierend auf einer Stärke von 1 Zoll gerendert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,5 </p></td> 
  <td class="stentry"> <p>Die dekale Breite und Höhe wird durch Katalog::Resolution bestimmt und ist ½ Zoll dick. </p></td> 
 </tr> 
</table>

## Verwandte Themen {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
