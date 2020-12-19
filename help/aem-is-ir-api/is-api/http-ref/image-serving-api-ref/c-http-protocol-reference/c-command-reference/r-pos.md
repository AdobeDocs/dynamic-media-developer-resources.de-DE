---
description: Ebenenposition.
seo-description: Ebenenposition.
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---


# pos{#pos}

Ebenenposition.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kohle</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der Herkunft dieser Ebene auf die Ebene 0 Herkunft (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Versatz von der Herkunft dieser Ebene zur Herkunft 0 der Ebene (real, real). </p></td> 
 </tr> 
</table>

Bei Bild-, Text- und Volltonfarbebenen gibt `pos=` die Position eines Ebenenankers relativ zum Ebenenanker 0 an. `posN=` Koordinatenwerte werden relativ zur tatsächlichen Ebene 0 rect normalisiert.

Bei Effektebenen verschiebt `pos=` die Effektebene relativ zur übergeordneten Ebene.

Positive Werte verschieben die Ebene nach rechts/unten, negativ nach links/oben. `posN=0.5,0.5` verschiebt die Ebene um die Hälfte der Ebene 0 Breite und Höhe nach unten und rechts.

## Eigenschaften {#section-51a60cdc52d040538fef378ace7c2e7d}

Ebenenattribut. Wird ignoriert, wenn `layer=0` oder `layer=comp`.

## Standard {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Dadurch wird der Ebenenanker an der gleichen Stelle wie der Ebenenanker 0 platziert, wenn es sich um eine Bild-, Text- oder Vollfarbebene handelt. Positioniert eine Effektebene direkt über oder unter der übergeordneten Ebene.

## Beispiel {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-812d95575ba542808e8387d0a8650606}

[herkunft=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
