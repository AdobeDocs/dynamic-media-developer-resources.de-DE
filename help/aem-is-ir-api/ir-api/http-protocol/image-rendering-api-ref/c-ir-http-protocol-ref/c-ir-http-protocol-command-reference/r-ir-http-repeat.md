---
description: Texturwiederholungsmodus. Gibt den Wiederholungsmodus für wiederholbare Texturmaterialien an.
seo-description: Texturwiederholungsmodus. Gibt den Wiederholungsmodus für wiederholbare Texturmaterialien an.
seo-title: wiederholen
solution: Experience Manager
title: wiederholen
topic: Scene7 Image Serving - Image Rendering API
uuid: 6508fdff-27cd-4038-b506-39b927f3526a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 16%

---


# wiederholen{#repeat}

Texturwiederholungsmodus. Gibt den Wiederholungsmodus für wiederholbare Texturmaterialien an.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Gleich wiederholen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4-Wege zufällige Kacheln. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8-Wege zufällige Kachelung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Diamantenfliese. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Quarter-Drop-Wallpaper hängen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Hintergrund </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Halbe Tropfen Tapete hängen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Fünfter-Tropfen-Tapete hängt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Hintergrundbild umkehren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Zufällige Hintergrundbilder hängen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>Zufälliger Tropfen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>Verdeckt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>Halb quer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>Spiegeln (Bookmatch). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>Standard-Randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>Hochfrequenz-Randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>Randomizer mit niedriger Frequenz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>Horizontaler Randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>Vertikaler Randomizer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Edge Randomizer. </p> </td> 
 </tr> 
</table>

Die zufälligen Quilting-Modi (14...18) können zur Synthese von Texturen aus Bildern verwendet werden, die nicht leicht wiederholbar sind. der Algorithmus erzeugt ganz zufällige oder teilweise zufällige Texturen, die auf dem Originalbild basieren.

## Eigenschaften {#section-262bf540930d4890b678ea00cefe1909}

Materialattribut. Die Materialien sind mit festen Farben, Dekormaterialien und Möbeln versehen.

## Standard {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, wenn das Material auf einem Katalogeintrag basiert, andernfalls  `0` (gerade Wiederholung).

## Verwandte Themen {#section-ac99113b64654d75a3a86e41db546269}

[Katalog::Repeat](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
