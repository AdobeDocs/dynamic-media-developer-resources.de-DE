---
description: Bild mit Ansicht ausrichten Richtet das zusammengesetzte Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des durch wid= und hei= definierten Ansichtsrechtecks aus.
solution: Experience Manager
title: align
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# align{#align}

Bild mit Ansicht ausrichten Richtet das zusammengesetzte Bild (möglicherweise nach der Skalierung, wenn auch scl= angegeben ist) innerhalb des durch wid= und hei= definierten Ansichtsrechtecks aus.

` align= *``*, *`horizvert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>horizontale Ausrichtung (real, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>vertikale Ausrichtung (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Geben Sie `align=-1,-1` an, um das Bild oben links im Bild mit der linken oberen Ecke der Ansicht auszurichten. Geben Sie `align=1,1` an, um das Bild unten, rechts, unten rechts neben der Ansicht auszurichten. Bei Standard-Bild- und Miniaturanfragen wird jeder Bereich der Ansicht, der nicht von zusammengesetzten Bilddaten abgedeckt wird, mit `bgc=` ausgefüllt.

## Eigenschaften {#section-3fbec8206fc944eda4746d8be84f3b41}

Attribut anzeigen. ( `align=` wird auch verwendet, um die Ausrichtung zwischen einem Wasserzeichenbild und dem Composite-Bild zu definieren, auf das das Wasserzeichen angewendet wird.) Gilt unabhängig von der aktuellen Ebeneneinstellung. Ignoriert , wenn nur einer von `wid=` und `hei=` angegeben ist und wenn `fit=constrain` oder `fit=stretch`.

## Standard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, wodurch das Bild im Rechteck der Ansicht zentriert wird.

## Beispiel {#section-2c9447aa2e184fb8ab1a4370dc61d554}

Die folgende Anforderung fügt `myImage` in ein 200 x 200 Pixel großes Ansichtsrechteck ein.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Wenn `myImage` genau quadratisch ist, wird das gesamte Ansichtsrechteck ausgefüllt. Wenn `myImage` ein Seitenverhältnis im Hochformat aufweist, wird es auf eine 200 Pixel hohe Skalierung skaliert und in der Ansicht horizontal zentriert. Wenn `myImage` ein Querformatseitenverhältnis aufweist, wird es auf eine Breite von 200 Pixel skaliert und an der oberen Kante der Ansicht ausgerichtet. In jedem Fall ist das zurückgegebene Bild genau 200 x 200 Pixel groß. Alle Leerzeichen, die nicht von der skalierten `myImage` abgedeckt werden, werden mit `attribute::BkgColor` gefüllt (geben Sie bgc= an, um die Hintergrundfarbe dynamisch zu steuern).

## Verwandte Themen {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Wasserzeichen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
