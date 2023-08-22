---
title: pos
description: Ebenenposition.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# pos{#pos}

Ebenenposition.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der Herkunft dieser Ebene zur Ebene 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Versatz von der Herkunft dieser Ebene zur Ebene 0 (real, real). </p></td> 
 </tr> 
</table>

Bei Bild-, Text- und einfarbigen Ebenen: `pos=` gibt die Position eines Ebenen-Ankers relativ zum Layer 0-Anker an. `posN=` Koordinatenwerte werden relativ zur tatsächlichen Ebene 0 rect size normalisiert.

Bei Effektschichten, `pos=` verschiebt die Effektebene relativ zur übergeordneten Ebene.

Positive Werte verschieben die Ebene nach rechts/unten, negative nach links/oben. `posN=0.5,0.5` verschiebt die Ebene um die Hälfte der Ebene 0 Breite und Höhe nach unten und rechts.

## Eigenschaften {#section-51a60cdc52d040538fef378ace7c2e7d}

Ebenenattribut. Ignoriert , wenn `layer=0` oder `layer=comp`.

## Standard {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Dadurch wird der Ebenenanker an derselben Position wie der Ebenen-0-Anker platziert, wenn es sich um eine Bild-, Text- oder Vollfarbschicht handelt. Positioniert eine Effektschicht direkt über oder unter ihrer übergeordneten Ebene.

## Beispiel {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
