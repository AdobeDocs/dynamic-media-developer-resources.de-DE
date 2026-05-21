---
title: anchor
description: Bild-Anker. Definiert den Ankerpunkt des Bildes, der Volltonfarbe oder des Rechtecks des Textbegrenzungsrahmens, bevor Transformationen angewendet werden (Zuschnitt=, Skalierung=, Drehen=, Spiegeln=). Dient auch als Drehmittelpunkt für Rotation=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
TQID: 'https://experienceleague.adobe.com/GKa8ChLxu85Wmi65uak7Kqn-Kme1GXL0FToaMAgHKoA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 2%

---

# anchor{#anchor}

Bild-Anker. Definiert den Ankerpunkt des Bildes, der Volltonfarbe oder des Rechtecks des Textbegrenzungsrahmens, bevor Transformationen angewendet werden (Zuschnitt=, Skalierung=, Drehen=, Spiegeln=). Dient auch als Drehmittelpunkt für Rotation=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Coord</span> </span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der linken oberen Ecke des Quellbilds (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>Normalisierter Versatz von der Mitte des Quellbilds (real, real) </p></td> 
 </tr> 
</table>

Der Ankerpunkt wird mit dem Bild transformiert und wird zum Ebenenursprungspunkt (sofern nicht auch `origin=` angegeben ist, in diesem Fall wird `anchor=` nur als Drehpunkt für `rotate=` verwendet).

`anchorN=0,0` platziert den Bildanker in der Mitte des Quellbilds. `anchorN=-0.5,-0.5` oder `anchor=0,0` befindet sich in der oberen linken Ecke und `anchorN=0.5,0.5` in der unteren rechten Ecke des Quellbilds.

## Eigenschaften {#section-f08942bc6aae46a8b5d341faaff80640}

Source-Bildattribut. Gilt für die aktuelle Ebene oder, falls `layer=comp`, für Ebene 0.

## Standard {#section-35d369fab1254f1a9b91684a6e169ad1}

Wenn `anchor=` nicht angegeben ist, wird catalog::anchor verwendet. Wenn `catalog::Anchor` nicht definiert ist, wird der Mittelpunkt des Bildrechtecks verwendet (genauso wie bei Angabe von `anchorN=0,0`).

Textebenen mit `textPs=` und Ebenen mit `clipPath=` können unterschiedliche Standardanker aufweisen.

## Beispiel {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Siehe „Beispiel C“ in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotation=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
