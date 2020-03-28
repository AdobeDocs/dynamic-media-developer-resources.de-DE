---
description: Bild mit Ansicht ausrichten Richtet das Composite-Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des Rechtecks der Ansicht, das durch wid= und hei= definiert wird.
seo-description: Bild mit Ansicht ausrichten Richtet das Composite-Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des Rechtecks der Ansicht, das durch wid= und hei= definiert wird.
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

Bild mit Ansicht ausrichten Richtet das Composite-Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des Rechtecks der Ansicht, das durch wid= und hei= definiert wird.

` align= *``*, *`horizvert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span></span> </p> </td> 
  <td class="stentry"> <p>horizontale Ausrichtung (real, -1.0..1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span></span> </p> </td> 
  <td class="stentry"> <p>vertikale Ausrichtung (real, -1.0..1.0) </p> </td> 
 </tr> 
</table>

Legen Sie `align=-1,-1` fest, ob das Composite-Bild oben links in der Ansicht ausgerichtet werden soll. Legen Sie fest, ob das Bild unten rechts neben der Ansicht ausgerichtet werden `align=1,1` soll. Bei Standardanfragen zum Erstellen von Bildern und Miniaturansichten werden alle Bereiche der Ansicht, die nicht durch zusammengesetzte Bilddaten abgedeckt sind, mit `bgc=`ausgefüllt.

## Eigenschaften {#section-3fbec8206fc944eda4746d8be84f3b41}

Ansicht. ( `align=` wird auch verwendet, um die Ausrichtung zwischen einem Wasserzeichenbild und dem Composite-Bild zu definieren, auf das das Wasserzeichen angewendet wird.) Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn nur einer von `wid=` und `hei=` angegeben ist und wenn `fit=constrain` oder `fit=stretch`.

## Standard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, wodurch das Ansicht im Rechteck zentriert wird.

## Beispiel {#section-2c9447aa2e184fb8ab1a4370dc61d554}

Die folgende Anforderung passt `myImage` in ein Rechteck mit 200 x 200 Pixel Ansicht.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Wenn `myImage` das Rechteck exakt quadratisch ist, wird das gesamte Rechteck der Ansicht gefüllt. Wenn `myImage` das Hochformat ein Seitenverhältnis aufweist, wird es auf eine Höhe von 200 Pixel skaliert und horizontal in der Ansicht zentriert. Wenn `myImage` das Querformat ein Seitenverhältnis hat, wird es auf eine Breite von 200 Pixel skaliert und am oberen Rand der Ansicht ausgerichtet. In allen Fällen ist das zurückgegebene Bild genau 200 x 200 Pixel groß. alle Bereiche, die nicht durch die Skalierung abgedeckt `myImage` werden, mit `attribute::BkgColor` (geben Sie bgc= an, um die Hintergrundfarbe dynamisch zu steuern).

## Verwandte Themen {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Wasserzeichen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
