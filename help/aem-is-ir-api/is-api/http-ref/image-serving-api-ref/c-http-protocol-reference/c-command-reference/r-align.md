---
title: align
description: Bild mit Ansicht ausrichten Richtet das zusammengesetzte Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des durch wid= und hei= definierten Ansichtsrechtecks aus.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# align{#align}

Bild mit Ansicht ausrichten Richtet das zusammengesetzte Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des durch wid= und hei= definierten Ansichtsrechtecks aus.

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>horizontale Ausrichtung (real, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>vertikale Ausrichtung (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Angeben `align=-1,-1` Um das Composite-Bild oben links in der Ansicht auszurichten, geben Sie `align=1,1` um das Bild unten rechts unten in der Ansicht auszurichten. Bei Standard-Bild- und Miniaturansichten wird jeder Bereich der Ansicht, der nicht von zusammengesetzten Bilddaten abgedeckt wird, mit `bgc=`.

## Eigenschaften {#section-3fbec8206fc944eda4746d8be84f3b41}

Attribut anzeigen. ( `align=` wird auch verwendet, um die Ausrichtung zwischen einem Wasserzeichenbild und dem zusammengesetzten Bild zu definieren, auf das das Wasserzeichen angewendet wird.) Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn nur einer von `wid=` und `hei=` festgelegt ist und wann `fit=constrain` oder `fit=stretch`.

## Standard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, wodurch das Bild im Rechteck der Ansicht zentriert wird.

## Beispiel {#section-2c9447aa2e184fb8ab1a4370dc61d554}

Die folgende Anfrage passt `myImage` in ein 200 x 200 Pixelansichtsrechteck.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Wenn `myImage` genau quadratisch ist, wird das gesamte Ansichtsrechteck gefüllt. Wenn `myImage` hat ein Seitenverhältnis im Hochformat, es wird auf 200 Pixel skaliert und horizontal in der Ansicht zentriert. Wenn `myImage` hat ein Querformatseitenverhältnis, es wird auf eine Breite von 200 Pixel skaliert und an der oberen Kante der Ansicht ausgerichtet. In jedem Fall ist das zurückgegebene Bild genau 200 x 200 Pixel groß; jeder Platz, der nicht von der skalierten abgedeckt wird `myImage` wird mit `attribute::BkgColor` (geben Sie bgc= an, um die Hintergrundfarbe dynamisch zu steuern).

## Verwandte Themen {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Wasserzeichen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
