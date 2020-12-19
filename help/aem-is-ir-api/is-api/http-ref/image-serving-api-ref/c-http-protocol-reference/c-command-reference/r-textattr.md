---
description: Attribute der Textebene. Gibt zusätzliche Attribute für Textebenen an, die nicht als RTF-Befehle verfügbar sind.
seo-description: Attribute der Textebene. Gibt zusätzliche Attribute für Textebenen an, die nicht als RTF-Befehle verfügbar sind.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---


# textAttr{#textattr}

Attribute der Textebene. Gibt zusätzliche Attribute für Textebenen an, die nicht als RTF-Befehle verfügbar sind.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>Bietet eine Möglichkeit zum Skalieren der Textebene, ohne die Schriftgröße zu ändern. Bei höheren Auflösungswerten wird die Größe des gerenderten Texts relativ zur Arbeitsflächengröße erhöht. kleinere Werte verringern die Textgröße. Textauflösung in Punkten pro Zoll (int größer als 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>Steuert den Anti-Aliasing-Modus, der von der Text-Rendering-Engine verwendet wird. </p> <p> <span class="codeph"> off | norm | knackig | scharf | stark | glatt  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> aus </span> </p> </td> 
      <td class="stentry"> <p>Deaktivieren Sie das Anti-Aliasing für Text. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
      <td class="stentry"> <p>Aktivieren Sie den standardmäßigen Anti-Aliasing-Modus für Text (Standard). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> crisp  </span> </p> </td> 
      <td class="stentry"> <p>Wählen Sie den Photoshop Anti-Aliasing-Modus <span class="codeph"> crisp </span> ( <span class="codeph"> nur textPs= </span>). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> spitze  </span> </p> </td> 
      <td class="stentry"> <p>Wählen Sie den Photoshop Anti-Aliasing-Modus <span class="codeph"> sharp </span> ( <span class="codeph"> Nur textPs= </span>). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Hoch </span> </p> </td> 
      <td class="stentry"> <p>Wählen Sie Photoshop Anti-Aliasing-Modus <span class="codeph"> strong </span> ( <span class="codeph"> nur textPs= </span>). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Steuert, wie beim Rendering des Textes die res verwendet werden </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>Verwenden Sie die angegebene Auflösung. </p> <p>Verwenden Sie diese Option, wenn der Text im Verhältnis zur Arbeitsfläche des Compositing exakt gerendert werden soll. Wenn das Textfeld zu klein ist, kann der Text auf die Ebenengröße geklickt werden (sofern angegeben). Dies ist die einzige Option <span class="varname"> resMode </span>, die von <span class="codeph"> textPs= </span> unterstützt wird. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>Passen Sie die Auflösung automatisch an, um den Ebenenrect am besten mit dem Text zu füllen. </p> <p>Verwenden Sie diese Option, um die Textgröße automatisch so anzupassen, dass das Textfeld so weit wie möglich gefüllt wird, ohne dass die Gefahr einer Kürzung besteht. Wenn die Zeilenumbruch aktiviert ist, kann der Text bei der endgültigen Auflösung umgebrochen werden. <span class="varname"> res  </span> wird ignoriert, wenn  <span class="codeph"> autoRes ausgewählt  </span> ist. Nicht unterstützt von <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>Verwenden Sie die angegebene Auflösung; gegebenenfalls verringern, um zu verhindern, dass Text auf den Ebenenrect abgeschnitten wird. </p> <p>Verwenden Sie diese Option, um Text mit der exakten angegebenen Auflösung zu rendern, solange kein Beschneiden erfolgt. Bei einer Beschneidung wird die Auflösung automatisch herabgesetzt, um sicherzustellen, dass der gesamte Text vollständig im Textfeld enthalten ist. Wenn die Zeilenumbruch aktiviert ist, kann der Text bei der endgültigen Auflösung umgebrochen werden. Nicht unterstützt von <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Wenn die Größe der Textebene nicht mit size= angegeben ist oder nur die Breite angegeben ist, werden die Einstellungen "autoRes"und "maxRes"ignoriert und die angegebene Auflösung wird zum Rendern des Textes verwendet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>Gibt den Umbruchmodus an. </p> <p> <span class="codeph"> wrap | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>Deaktivieren Sie Wortumbruch. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> umbruch </span> </p> </td> 
      <td class="stentry"> <p>Standard-Wortumbruch aktivieren </p> <p>Bricht bei Bedarf lange Wörter. <span class="codeph"> textPs= unterstützt  </span> nur  <span class="codeph"> Wrap  </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>Umbruch aktivieren </p> <p>Zerbricht nie ein Wort, auch wenn es am Ende abgeschnitten wird. Wird normalerweise zusammen mit <span class="codeph"> autoRes </span> oder <span class="codeph"> maxRes </span> verwendet, um sicherzustellen, dass lange Wörter nicht beschädigt werden. </p> </td> 
     </tr> 
    </table> </p> <p>Sowohl <span class="codeph"> umschließen </span> als auch <span class="codeph"> nbwrap </span> wird automatisch auf Wortgrenzen und Bindestriche umgebrochen. </p> </td> 
 </tr> 
</table>

## Eigenschaften {#section-114ca0b8585b403c873e2251478ad1d5}

Textebenenattribut. Ignoriert durch Bild-, Farbton- und Effektebenen. Gilt für `layer=0`, wenn für `layer=comp` angegeben.

## Standard {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Verwandte Themen {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
