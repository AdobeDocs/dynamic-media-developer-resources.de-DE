---
title: wiederholen
description: Textur - Wiederholungsmodus. Gibt den Wiederholungsmodus für wiederholbare Texturmaterialien an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6cc82742-4ba0-4524-a87b-586539d7fe38
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 16%

---

# wiederholen{#repeat}

Textur - Wiederholungsmodus. Gibt den Wiederholungsmodus für wiederholbare Texturmaterialien an.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Gerade Wiederholung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4-Wege-Fliesen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8-Wege-Fliesen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Diamantfliesen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Quarter-Drop Tapete hängt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Third-Drop Tapete hängt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Half-Drop Tapete hängt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Fifth-drop Tapete hängt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Umgekehrte Tapete hängt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Zufällige Tapeten hängen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>Zufälliger Absturz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>Zufällig verteilt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>Halb quer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>Mirror (Buchvergleich). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>Standard-Randomisierer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>Hochfrequenz-Randomisierer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>Niederfrequenz-Randomisierer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>Horizontaler Randomisierer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>Vertikaler Randomisierer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Edge Randomizer. </p> </td> 
 </tr> 
</table>

Die zufälligen Steppmodi (14…18) können verwendet werden, um Texturen aus Bildern zu erzeugen, die nicht ohne weiteres wiederholbar sind; der Algorithmus erzeugt vollständig zufällige oder teilweise zufällige Texturen basierend auf dem Originalbild.

## Eigenschaften {#section-262bf540930d4890b678ea00cefe1909}

Materialattribut. Wird von einfarbigen Abziehbildern und Schrankmaterialien ignoriert.

## Standard {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, wenn das Material auf einem Katalogeintrag basiert, andernfalls `0` (gerade Wiederholung).

## Verwandte Themen {#section-ac99113b64654d75a3a86e41db546269}

[catalog:repeat](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
