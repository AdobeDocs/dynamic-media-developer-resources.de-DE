---
description: Farbwerte. Sie können Farbwerte entweder mit Hexadezimalnotation, einer kommagetrennten Liste von Komponentenwerten oder Dezimalzahlen angeben.
solution: Experience Manager
title: Farbe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 2ff380ad30911a85bc066ae53f0cb69360ed99e4
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 3%

---

# Farbe{#color}

Farbwerte. Sie können Farbwerte entweder mit Hexadezimalnotation, einer kommagetrennten Liste von Komponentenwerten oder Dezimalzahlen angeben.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Farbe</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&amp;lub;&amp;lub;<span class="varname"> grau</span>[,<span class="varname"> alpha</span>][g]&amp;rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> rot</span>,<span class="varname"> grün</span>,<span class="varname"> blau</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>, <span class="varname"> magenta</span>, <span class="varname"> gelb</span>, <span class="varname"> schwarz</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}&amp;rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rot</span>, <span class="varname"> grün</span>, <span class="varname"> blau</span>, <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>Wert der Farbkomponente (0…255, decimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Cyan</span>, <span class="varname"> Magenta</span>, <span class="varname"> Gelb</span>, <span class="varname"> Schwarz</span>, <span class="varname"> Alpha</span></span> </p></td> 
  <td class="stentry"> <p>CMYK-Farbkomponentenwert (0..100 %, Dezimalint) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Grau</span>, <span class="varname"> Alpha</span></span> </p> </td> 
  <td class="stentry"> <p>Wert der grauen Farbkomponente (0…100 %, Dezimalzahl int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>gepackter zweistelliger hex-grauer Farbwert (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> HEX4</span> </span> </p> </td> 
  <td class="stentry"> <p>Verpackt vierstellig hex grau mit Alpha-Farbwert (GGA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>Gepackter sechsstelliger hexadezimaler RGB-Farbwert (RGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>Gepackter achtstelliger hexadezimaler RGBA- (RGGBBAA) oder CMYK- (CCMMYKK) Farbwert (wenn mit dem Suffix 'k' angegeben) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> HEX10</span> </span> </p></td> 
  <td class="stentry"> <p>gepacktes zehnstelliges hexadezimales CMYK mit Alpha-Wert (CCYMMKKAA) </p> </td> 
 </tr> 
</table>

Die Dezimalkomponentenwerte für RGB-Farben liegen im Bereich 0 bis 255. Die Dezimalkomponentenwerte für CMYK und Grau liegen im Bereich 0 bis 100 %. Alle Hexadezimalkomponentenwerte liegen im Bereich 0…0xFF.

Farbkomponentenwerte werden als unabhängig vom Alpha-Wert angenommen (nicht vormultipliziert).

Bei allen Farbwerten, Präfixen und Suffixen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Für CMYK-Farbwerte ist das Typsuffix &#39;k&#39; erforderlich. Ein Typsuffix kann optional für RGB- und Grauwerte angegeben werden.

Das Präfix &#39;0x&#39; ist für hexadezimale Grauwerte erforderlich.

Das Suffix &#39;s&#39; gibt an, dass der Farbwert mit dem Farbraum der Eingabe (Quelle) verbunden ist, der dem Pixeltyp des Farbwerts entspricht (definiert mit `attribute::IccProfileSrc*`). Wenn dieses Suffix nicht vorhanden ist, wird der Farbwert mit dem Ausgabefarbraum (Ziel) verknüpft (definiert mit `icc=` oder `attribute::IccProfile*`).

## Standard {#section-737082a7da544acca8092a48d88480e7}

Wenn ein Alpha-Wert nicht explizit angegeben wird, wird von 255, 0xFF oder 100 % ausgegangen (vollständig opak).

## Beispiele {#section-4ac69026349949f8b595a6d4a9ce474d}

Einige Beispiele für gültige Farbspezifikatoren und ihren entsprechenden Pixeltyp, Farbwert, Alpha-Wert und Standardfarbraum:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Pixeltyp</b> </th> 
   <th class="entry"> <b>Farbwert</b> </th> 
   <th class="entry"> <b>Alpha-Wert</b> </th> 
   <th class="entry"> <b>Standardfarbraum </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRGB</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0 100 200 200 RS </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160.177.194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRGB</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>hundert </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75 g </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>50 % </p> </td> 
   <td> <p>75 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x70g </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>87 % </p> </td> 
   <td> <p>93 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray-</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94 11 50 33 K </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94 11 50 33 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22 23 24 25 % </p> </td> 
   <td> <p>26 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56 57 58 59 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Der mit `icc=` angegebene Ausgabefarbraum gilt anstelle des Standardfarbraums, wenn der Pixeltyp einer Ausgabefarbe dem Pixeltyp des Ausgabebilds entspricht.
