---
title: textAttr
description: Textebenenattribute. Gibt zusätzliche Attribute für Textebenen an, die nicht als RTF-Befehle verfügbar sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

Textebenenattribute. Gibt zusätzliche Attribute für Textebenen an, die nicht als RTF-Befehle verfügbar sind.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Es bietet eine Möglichkeit, die Textebene zu skalieren, ohne die Schriftgrößen zu ändern. Höhere Auflösungswerte erhöhen die Größe des gerenderten Textes im Verhältnis zur Arbeitsflächengröße. Kleinere Werte verringern die Textgröße. Textauflösung in Punkten pro Zoll (int größer als 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> AntiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>Steuert den Anti-Aliasing-Modus, der von der Text-Rendering-Engine verwendet wird. </p> <p> <span class="codeph"> | Norm | knackig | stechend | kräftig | </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> von </span> </p> </td> 
      <td class="stentry"> <p>Deaktivieren Sie Text-Anti-Aliasing. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">-</span> </p> </td> 
      <td class="stentry"> <p>Standardmodus für Text-Anti-Aliasing aktivieren (Standard). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> knackige </span> </p> </td> 
      <td class="stentry"> <p>Wählen Sie den Anti-Aliasing-Modus von Photoshop <span class="codeph"> gestochen scharfe </span> aus (nur <span class="codeph"> textPs= </span>). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> scharfer </span> </p> </td> 
      <td class="stentry"> <p>Wählen Sie den Kantenglättungsmodus von Photoshop <span class="codeph"> scharfe </span> aus (nur <span class="codeph"> textPs= </span>). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> starker </span> </p> </td> 
      <td class="stentry"> <p>Wählen Sie den Photoshop-Anti-Aliasing-Modus <span class="codeph"> starke </span> aus (nur <span class="codeph"> textPs= </span>). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Steuert, wie res beim Rendern des Textes verwendet wird </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes-</span> </p> </td> 
      <td class="stentry"> <p>Verwendet die angegebene Auflösung. </p> <p>Verwenden Sie , wenn der Text in einer exakten Größe relativ zur zusammengesetzten Arbeitsfläche gerendert werden soll. Text kann auf die Ebenengröße (falls angegeben) abgeschnitten werden, wenn das Textfeld zu klein ist. Dies ist die einzige <span class="varname"> resMode-</span>, die von <span class="codeph"> textPs= </span> unterstützt wird. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes-</span> </p> </td> 
      <td class="stentry"> <p>Passen Sie die Auflösung automatisch an, um die Ebene am besten mit dem Text zu füllen. </p> <p>Verwenden Sie , um die Textgröße so anzupassen, dass das Textfeld so gut wie möglich ausgefüllt wird, ohne dass die Gefahr eines Abschnitts besteht. Wenn der Zeilenumbruch aktiviert ist, kann der Text in der endgültigen Auflösung neu umgebrochen werden. Die <span class="varname">-</span> wird ignoriert, wenn <span class="codeph"> autoRes-</span> ausgewählt ist. Wird von <span class="codeph"> textPs= </span> nicht unterstützt. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes-</span> </p> </td> 
      <td class="stentry"> <p>Verwenden Sie die angegebene Auflösung. Verringern Sie sie bei Bedarf, um zu verhindern, dass Text auf die Ebene gekürzt wird. </p> <p>Verwendet, um Text mit der angegebenen Auflösung zu rendern, solange kein Clipping erfolgt. Beim Beschneiden wird die Auflösung automatisch verringert, um sicherzustellen, dass der gesamte Text vollständig im Textfeld enthalten ist. Wenn der Zeilenumbruch aktiviert ist, kann der Text in der endgültigen Auflösung neu umgebrochen werden. Wird von <span class="codeph"> textPs= </span> nicht unterstützt. </p> </td> 
     </tr> 
    </table> </p> <p>Wenn die Größe der Textebene nicht mit size= angegeben ist oder nur die Breite angegeben ist, werden die Einstellungen „autoRes“ und „maxRes“ ignoriert. In solchen Fällen wird die angegebene Auflösung zum Rendern des Textes verwendet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> WordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Gibt den Umbruchmodus an. </p> <p> <span class="codeph"> | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Zeilenumbruch deaktivieren. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Wrap </span> </p> </td> 
      <td class="stentry"> <p>Standardmäßige Zeilenumbrüche aktivieren. </p> <p>Er bricht lange Worte, wenn nötig. <span class="codeph"> textPs= </span> unterstützt nur <span class="codeph"> Wrap-</span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Aktivieren Sie den unterbrechungsfreien Zeilenumbruch. </p> <p>bricht nie ein Wort, auch wenn es am Ende abgeschnitten wird. Wird normalerweise mit <span class="codeph"> autoRes-</span> oder <span class="codeph"> maxRes-</span> verwendet, um sicherzustellen, dass lange Wörter nie gebrochen werden. </p> </td> 
     </tr> 
    </table> </p> <p>Sowohl <span class="codeph"> </span> als auch <span class="codeph"> nbwrap </span> automatisch an Wortgrenzen und Bindestrichen umgebrochen. </p> </td> 
 </tr> 
</table>

## Eigenschaften {#section-114ca0b8585b403c873e2251478ad1d5}

Attribut der Textebene. Wird von Bild-, Vollbild- und Effektebenen ignoriert. Gilt für `layer=0`, wenn für `layer=comp` angegeben.

## Standard {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Verwandte Themen {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
