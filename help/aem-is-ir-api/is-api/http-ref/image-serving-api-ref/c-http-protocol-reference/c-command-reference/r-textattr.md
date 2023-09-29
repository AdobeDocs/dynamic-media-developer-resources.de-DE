---
title: textAttr
description: Attribute der Textebene. Gibt zusätzliche Attribute für Textebenen an, die nicht als rtf-Befehle verfügbar sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 1%

---

# textAttr{#textattr}

Attribute der Textebene. Gibt zusätzliche Attribute für Textebenen an, die nicht als rtf-Befehle verfügbar sind.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Es bietet eine Möglichkeit, die Textebene zu skalieren, ohne die Schriftgröße zu ändern. Höhere Auflösungswerte erhöhen die Größe des gerenderten Texts relativ zur Arbeitsflächengröße, kleinere Werte verringern die Textgröße. Textauflösung in Punkten pro Zoll (int größer als 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>Steuert den Anti-Aliasing-Modus, der von der Text-Rendering-Engine verwendet wird. </p> <p> <span class="codeph"> off | norm | knackig | scharf | stark | glatt </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> aus </span> </p> </td> 
      <td class="stentry"> <p>Deaktivieren Sie das Anti-Aliasing von Text. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
      <td class="stentry"> <p>Aktivieren Sie den standardmäßigen Anti-Aliasing-Modus für Text (Standard). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> crisp </span> </p> </td> 
      <td class="stentry"> <p>Photoshop-Anti-Aliasing-Modus auswählen <span class="codeph"> crisp </span> ( <span class="codeph"> textPs= </span> nur). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> scharf </span> </p> </td> 
      <td class="stentry"> <p>Photoshop-Anti-Aliasing-Modus auswählen <span class="codeph"> scharf </span> ( <span class="codeph"> textPs= </span> nur). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> stark </span> </p> </td> 
      <td class="stentry"> <p>Photoshop-Anti-Aliasing-Modus auswählen <span class="codeph"> stark </span> ( <span class="codeph"> textPs= </span> nur). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Steuert die Verwendung von res beim Rendern des Texts </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Verwenden Sie die angegebene Auflösung. </p> <p>Verwenden Sie diese Option, wenn der Text im Verhältnis zur zusammengesetzten Arbeitsfläche in exakter Größe dargestellt werden soll. Wenn das Textfeld zu klein ist, kann der Text auf die Ebenengröße gekürzt werden (sofern angegeben). Dies ist die einzige <span class="varname"> resMode </span> -Option unterstützt von <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Passen Sie die Auflösung automatisch an, um den Ebenenrect am besten mit dem Text zu füllen. </p> <p>Verwenden Sie , um die Textgröße automatisch so anzupassen, dass das Textfeld so weit wie möglich gefüllt wird, ohne dass die Gefahr einer Kürzung besteht. Wenn die Wortumbruchfunktion aktiviert ist, kann der Text bei der endgültigen Auflösung umgebrochen werden. Die <span class="varname"> res </span> wird ignoriert, wenn <span class="codeph"> autoRes </span> ausgewählt ist. Nicht unterstützt von <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Verwenden Sie die angegebene Auflösung. Verringern Sie sie bei Bedarf, um zu verhindern, dass Text auf das Ebenenrect abgeschnitten wird. </p> <p>Verwenden Sie , um Text mit der angegebenen Auflösung zu rendern, solange kein Beschneiden erfolgt. Bei Beschneidungen wird die Auflösung automatisch herabgesetzt, um sicherzustellen, dass der gesamte Text vollständig im Textfeld enthalten ist. Wenn die Wortumbruchfunktion aktiviert ist, kann der Text bei der endgültigen Auflösung umgebrochen werden. Nicht unterstützt von <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Wenn die Größe der Textebene nicht mit size= angegeben ist oder nur die Breite angegeben ist, werden die Einstellungen "autoRes"und "maxRes"ignoriert. In solchen Fällen wird die angegebene Auflösung zum Rendern des Textes verwendet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Gibt den Wrapping-Modus an. </p> <p> <span class="codeph"> wrap | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Wortumbruch deaktivieren. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> umbruch </span> </p> </td> 
      <td class="stentry"> <p>Standard-Wortumbruch aktivieren. </p> <p>Es bricht bei Bedarf lange Wörter. <span class="codeph"> textPs= </span> nur unterstützt <span class="codeph"> wrap </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Aktivieren Sie die unterbrechungsfreie Wortumbruchfunktion. </p> <p>Zerbricht nie ein Wort, selbst wenn es am Ende abgeschnitten wird. Wird normalerweise mit <span class="codeph"> autoRes </span> oder <span class="codeph"> maxRes </span> um sicherzustellen, dass lange Wörter nie gebrochen werden. </p> </td> 
     </tr> 
    </table> </p> <p>Beide <span class="codeph"> wrap </span> und <span class="codeph"> nbwrap </span> automatisch auf Wortgrenzen und Bindestriche umschließen. </p> </td> 
 </tr> 
</table>

## Eigenschaften {#section-114ca0b8585b403c873e2251478ad1d5}

Textebenenattribut. Ignoriert von Bild-, Farb- und Effektebenen. Gilt für `layer=0` sofern für `layer=comp`.

## Standard {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Verwandte Themen {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
