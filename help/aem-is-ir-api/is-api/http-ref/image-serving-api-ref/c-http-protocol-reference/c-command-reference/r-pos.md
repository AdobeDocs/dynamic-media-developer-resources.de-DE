---
title: POS
description: Ebenenposition.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
TQID: 'https://experienceleague.adobe.com/9UMGN0TeM4mZ0IZI--dEA3KBYKOVhJxCJMZuPevlq8o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 2%

---

# POS{#pos}

Ebenenposition.

Pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset vom Ursprung dieser Ebene zum Ursprung der Ebene 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Versatz vom Ursprung dieser Ebene zum Ursprung der Ebene 0 (real, real). </p></td> 
 </tr> 
</table>

Bei Bild-, Text- und Volltonfarbschichten gibt `pos=` die Position eines Ebenenankers relativ zum Ebene 0-Anker an. Die `posN=` Koordinatenwerte werden relativ zur tatsächlichen Größe der Ebene 0 (rect size) normalisiert.

Wenn Effektebenen vorhanden sind, verschiebt `pos=` die Effektebene relativ zur übergeordneten Ebene.

Positive Werte verschieben die Ebene nach rechts/unten und negative nach links/oben. In `posN=0.5,0.5` wird die Ebene um die Hälfte der Breite und Höhe der Ebene 0 nach unten und rechts verschoben.

## Eigenschaften {#section-51a60cdc52d040538fef378ace7c2e7d}

Ebenenattribut. Ignoriert, wenn `layer=0` oder `layer=comp`.

## Standard {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Diese Koordinate platziert den Ebenenanker an derselben Position wie den Ebenenanker 0, wenn es sich um eine Bild-, Text- oder einfarbige Ebene handelt. Positioniert eine Effektebene direkt über oder unter der übergeordneten Ebene.

## Beispiel {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-812d95575ba542808e8387d0a8650606}

[Herkunft=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
