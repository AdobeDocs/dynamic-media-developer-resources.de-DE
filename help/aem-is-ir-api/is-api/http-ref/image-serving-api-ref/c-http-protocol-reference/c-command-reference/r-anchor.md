---
title: anchor
description: Bildanker. Definiert den Ankerpunkt des Rechtecks für Bild, Farbe oder Textbegrenzungsrahmen, bevor die Transformationen angewendet werden (Zuschneiden=, Skalieren=, Drehen=, Spiegeln=, Spiegeln=). Dient auch als Drehmittelpunkt für rotate=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# anchor{#anchor}

Bildanker. Definiert den Ankerpunkt des Rechtecks für Bild, Farbe oder Textbegrenzungsrahmen, bevor die Transformationen angewendet werden (Zuschneiden=, Skalieren=, Drehen=, Spiegeln=, Spiegeln=). Dient auch als Drehmittelpunkt für rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelversatz von der oberen linken Ecke des Quellbilds (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>normalisierte Verschiebung von der Mitte des Quellbilds (real, real) </p></td> 
 </tr> 
</table>

Der Verankerungspunkt wird mit dem Bild transformiert und wird zum Ebenenursprungspunkt (sofern `origin=` auch angegeben ist, in welchem Fall `anchor=` wird nur als Drehmittelpunkt für `rotate=`).

`anchorN=0,0` platziert den Bildanker in der Mitte des Quellbilds. `anchorN=-0.5,-0.5` oder `anchor=0,0` befindet sich oben links und `anchorN=0.5,0.5` befindet sich in der rechten unteren Ecke des Quellbilds.

## Eigenschaften {#section-f08942bc6aae46a8b5d341faaff80640}

Quellbildattribut. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`.

## Standard {#section-35d369fab1254f1a9b91684a6e169ad1}

Wenn `anchor=` nicht angegeben ist, wird catalog::Anchor verwendet. Wenn `catalog::Anchor` nicht definiert ist, wird die Mitte des Bildrechtecks verwendet (entspricht der Angabe von `anchorN=0,0`).

Textebenen mit `textPs=` und Ebenen, die `clipPath=` kann über verschiedene Standardanker verfügen.

## Beispiel {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Siehe &quot;Beispiel C&quot;in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog:Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
