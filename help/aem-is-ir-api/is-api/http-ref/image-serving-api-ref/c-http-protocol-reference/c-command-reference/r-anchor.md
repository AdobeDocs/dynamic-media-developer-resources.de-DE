---
description: Bildanker. Definiert den Verankerungspunkt des Bilds, der Volltonfarbe oder des Rechtecks des Textbegrenzungsrahmens, bevor die Transformationen angewendet werden (Beschneiden=, Skalieren=, Drehen=, Flip=). Dient auch als Mittelpunkt der Drehung für rotate=.
seo-description: Bildanker. Definiert den Verankerungspunkt des Bilds, der Volltonfarbe oder des Rechtecks des Textbegrenzungsrahmens, bevor die Transformationen angewendet werden (Beschneiden=, Skalieren=, Drehen=, Flip=). Dient auch als Mittelpunkt der Drehung für rotate=.
seo-title: anchor
solution: Experience Manager
title: anchor
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# anchor{#anchor}

Bildanker. Definiert den Verankerungspunkt des Bilds, der Volltonfarbe oder des Rechtecks des Textbegrenzungsrahmens, bevor die Transformationen angewendet werden (Beschneiden=, Skalieren=, Drehen=, Flip=). Dient auch als Mittelpunkt der Drehung für rotate=.

`anchor= *`Kohle`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Buchse</span></span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke des Quellbilds (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> AkkordN</span></span> </p> </td> 
  <td class="stentry"> <p>normalisierter Offset vom Mittelpunkt des Quellbilds (real, real) </p></td> 
 </tr> 
</table>

Der Ankerpunkt wird mit dem Bild transformiert und wird zum Ebenenrichtpunkt (es sei denn, es `origin=` wird auch angegeben. In diesem Fall `anchor=` wird nur der Mittelpunkt der Drehung verwendet `rotate=`).

`anchorN=0,0` platziert den Bildanker in der Mitte des Quellbilds. `anchorN=-0.5,-0.5` oder `anchor=0,0` befindet sich in der oberen linken Ecke und `anchorN=0.5,0.5` befindet sich in der unteren rechten Ecke des Quellbilds.

## Eigenschaften {#section-f08942bc6aae46a8b5d341faaff80640}

Quellenbildattribut. Gilt für die aktuelle Ebene oder für die Ebene 0, wenn `layer=comp`.

## Standard {#section-35d369fab1254f1a9b91684a6e169ad1}

Wenn `anchor=` kein Wert angegeben ist, wird catalog::Anchor verwendet. Wenn `catalog::Anchor` nicht definiert ist, wird die Mitte des Bildrechtecks verwendet (genau wie bei der Angabe `anchorN=0,0`).

Textebenen, an denen `textPs=` und Ebenen beteiligt sind, `clipPath=` können unterschiedliche Standardanker haben.

## Beispiel {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Siehe &quot;Beispiel C&quot;in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [Herkunft=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
