---
title: Größe
description: Abziehbildgröße. Breite, Höhe und Dicke eines Abziehbildobjekts.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
TQID: 'https://experienceleague.adobe.com/HLyEmmOch9kiHQ3sqpvHCQiHOBltjQcsZaDu0na1-Ww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 5%

---

# Größe{#size}

Abziehbildgröße. Breite, Höhe und Dicke eines Abziehbildobjekts.

## Eigenschaften {#section-967bf1112eec4032a91ed0c8a7b10a07}

Drei reelle Zahlen, durch Kommas getrennt. Sie darf nicht negativ sein. Legen Sie nicht verwendete Werte auf 0 fest. Nachfolgende Nullen können weggelassen werden.

Geben Sie sowohl Breite als auch Höhe nur an, wenn das Bild so gedehnt werden soll, dass es der angegebenen Größe entspricht (das Seitenverhältnis kann sich ändern). Legen Sie entweder Breite oder Höhe fest, um das Bild proportional zu skalieren. Legen Sie sowohl Breite als auch Höhe auf 0 fest, um `catalog::Resolution`zur Bestimmung der Objektgröße zu verwenden.

Geben Sie einen Wert für die Dicke an, um dem Abziehbild-Objekt einen Schlagschatten hinzuzufügen. Optional für Abziehbildmaterialien, von allen anderen Materialien ignoriert.

## Standard {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Dies bedeutet, dass die Abziehbildgröße anhand von catalog:resolution bestimmt werden muss und dass das Objekt keine Dicke aufweist (daher wird kein Schlagschatten gerendert).

## Beispiele {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>Das Abziehbild wird auf 12x3 Zoll in der Größe erzwungen und hat keine Dicke (dies ist kein Tropfenschatten). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>Das Abziehbild ist 5 Zoll breit, die Höhe wird durch das Seitenverhältnis des Bildes bestimmt und ein Schlagschatten wird basierend auf einer 1-Zoll-Dicke gerendert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>Die Breite und Höhe des Abziehbilds wird durch „catalog:Resolution“ festgelegt und durch die Dicke des Abziehbilds von ½ Zoll bestimmt. </p></td> 
 </tr> 
</table>

## Verwandte Themen {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog:Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

