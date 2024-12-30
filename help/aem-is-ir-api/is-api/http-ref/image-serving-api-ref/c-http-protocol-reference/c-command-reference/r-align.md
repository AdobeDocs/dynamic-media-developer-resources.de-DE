---
title: in eine Linie bringen
description: Bild an Ansicht ausrichten. Richtet das zusammengesetzte Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des durch wid= und hei= definierten Ansichtsrechtecks aus.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# in eine Linie bringen{#align}

Bild an Ansicht ausrichten. Richtet das zusammengesetzte Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des durch wid= und hei= definierten Ansichtsrechtecks aus.

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>Horizontale Ausrichtung (real, -1,0…1,0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>Vertikale Ausrichtung (real, -1,0…1,0) </p> </td> 
 </tr> 
</table>

Geben Sie `align=-1,-1` an, um die obere linke Seite des zusammengesetzten Bildes mit der oberen linken Seite der Ansicht auszurichten, geben Sie `align=1,1` an, um die untere rechte Seite des Bildes mit der unteren rechten Seite der Ansicht auszurichten. Bei Standardanfragen für Bilder und Miniaturen werden alle Bereiche der Ansicht, die nicht von zusammengesetzten Bilddaten abgedeckt werden, mit `bgc=` gefüllt.

## Eigenschaften {#section-3fbec8206fc944eda4746d8be84f3b41}

Attribut anzeigen. ( `align=` wird auch verwendet, um die Ausrichtung zwischen einem Wasserzeichenbild und dem zusammengesetzten Bild zu definieren, auf das das Wasserzeichen angewendet wird.) Wird unabhängig von der aktuellen Ebeneneinstellung angewendet. Ignoriert, wenn nur eines von `wid=` und `hei=` angegeben ist und wenn `fit=constrain` oder `fit=stretch`.

## Standard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, das das Bild im Rechteck zentriert.

## Beispiel {#section-2c9447aa2e184fb8ab1a4370dc61d554}

Die folgende Anfrage passt `myImage` in ein Rechteck mit einer Ansicht von 200 x 200 Pixel.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Wenn `myImage` exakt quadratisch ist, füllt es das gesamte Ansichtsrechteck. Wenn `myImage` ein Seitenverhältnis im Hochformat aufweist, wird es auf eine Höhe von 200 Pixel skaliert und in der Ansicht horizontal zentriert. Wenn `myImage` ein Querformat-Seitenverhältnis aufweist, wird es auf eine Breite von 200 Pixeln skaliert und an der oberen Kante der Ansicht ausgerichtet. In allen Fällen ist das zurückgegebene Bild genau 200x200 Pixel groß; jeder Bereich, der nicht von der skalierten `myImage` abgedeckt wird, ist mit `attribute::BkgColor` gefüllt (geben Sie bgc= an, um die Hintergrundfarbe dynamisch zu steuern).

## Verwandte Themen {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
