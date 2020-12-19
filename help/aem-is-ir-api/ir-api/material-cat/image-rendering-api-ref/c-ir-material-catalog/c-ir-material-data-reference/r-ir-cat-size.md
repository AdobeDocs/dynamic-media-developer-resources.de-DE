---
description: Dezimalgröße. Breite, Höhe und Dicke eines dekalen Materialobjekts.
seo-description: Dezimalgröße. Breite, Höhe und Dicke eines dekalen Materialobjekts.
seo-title: Größe
solution: Experience Manager
title: Größe
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 5%

---


# Größe{#size}

Dezimalgröße. Breite, Höhe und Dicke eines dekalen Materialobjekts.

## Eigenschaften {#section-967bf1112eec4032a91ed0c8a7b10a07}

Drei durch Kommas getrennte reale Zahlen. Darf nicht negativ sein. Legen Sie nicht verwendete Werte auf 0 fest. Nachfolgende Nullen können weggelassen werden.

Geben Sie nur dann Breite und Höhe an, wenn das Bild so gestreckt werden soll, dass es an die angegebene Größe angepasst wird (das Seitenverhältnis kann sich ändern). Legen Sie entweder Breite oder Höhe fest, um das Bild proportional zu skalieren. Legen Sie Breite und Höhe auf 0 fest, um `catalog::Resolution`die Objektgröße zu bestimmen.

Geben Sie einen Dickenwert ein, um dem Dekorobjekt einen Schlagschatten hinzuzufügen. Optional für dekale Materialien, die von allen anderen Materialien ignoriert werden.

## Standard {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Dies bedeutet, dass die Größe des Dezimalzeichens anhand von catalog::Resolution bestimmt werden soll und dass das Objekt keine Stärke hat (daher wird kein Schlagschatten gerendert).

## Beispiele {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>Der Abfall ist auf 12x3 Zoll in der Größe und hat keine Dicke (das heißt, kein Schlagschatten). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>Der Abstufungsgrad ist 5 Zoll breit, die Höhe wird durch das Seitenverhältnis des Bildes bestimmt und ein Schlagschatten wird basierend auf einer Stärke von 1 Zoll gerendert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,,5 </p></td> 
  <td class="stentry"> <p>Die dekale Breite und Höhe wird durch Katalog::Resolution bestimmt und ist ½ Zoll dick. </p></td> 
 </tr> 
</table>

## Verwandte Themen {#section-31a164e781d14e92bd9d379d3c329e92}

[Katalog:Auflösung](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
