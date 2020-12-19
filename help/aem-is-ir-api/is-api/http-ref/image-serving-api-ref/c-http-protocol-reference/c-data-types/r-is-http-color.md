---
description: Farbwerte. Sie können Farbwerte entweder mit hexadezimaler Notation, einer kommagetrennten Liste von Komponentenwerten oder mit Dezimalstellen angeben.
seo-description: Farbwerte. Sie können Farbwerte entweder mit hexadezimaler Notation, einer kommagetrennten Liste von Komponentenwerten oder mit Dezimalstellen angeben.
seo-title: Farbe
solution: Experience Manager
title: Farbe
topic: Scene7 Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 14%

---


# color{#color}

Farbwerte. Sie können Farbwerte entweder mit hexadezimaler Notation, einer kommagetrennten Liste von Komponentenwerten oder mit Dezimalstellen angeben.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> grau</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>,  <span class="varname"> magenta</span>,  <span class="varname"> gelb</span>,  <span class="varname"> schwarz</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rot</span>,  <span class="varname"> grün</span>,  <span class="varname"> blau</span>,  <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>color component value (0...255, decimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Cyan</span>,  <span class="varname"> Magenta</span>,  <span class="varname"> Gelb</span>,  <span class="varname"> Schwarz</span>,  <span class="varname"> Alpha</span></span> </p></td> 
  <td class="stentry"> <p>CMYK-Farbkomponentenwert (0,100 %, Dezimalzahl) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> grau</span>,  <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>Wert der grauen Farbkomponente (0...100%, Dezimalzahl) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>gepackter zweistelliger hexadezimaler Farbwert (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>4-stellige Hex gray mit Alpha-Farbwert (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>Sechstelliger hexadezimaler RGB-Farbwert (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>8-stelliger hexadezimaler RGBA- (RRGGBBAA) oder CMYK- (CCMMYKK-) Farbwert (falls mit dem Suffix 'k' angegeben) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>Zehn-stellige hexadezimale CMYK mit Alphawert (CCYMMKAA) </p> </td> 
 </tr> 
</table>

Die Werte der Dezimalkomponenten für RGB-Farben liegen im Bereich 0...255. Dezimalkomponentenwerte für CMYK und Grau liegen im Bereich von 0,100%. Alle hexadezimalen Komponentenwerte liegen im Bereich 0...0xFF.

Farbkomponentenwerte werden als unabhängig vom Alpha-Wert (nicht vormultipliziert) angenommen.

Bei allen Farbwerten, Präfixen und Suffixen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Das Typsuffix &#39;k&#39; ist für CMYK-Farbwerte erforderlich. Ein Typsuffix kann optional für RGB- und Graufarbwerte angegeben werden.

Das Präfix &quot;0x&quot;ist für hexadezimale graue Farbwerte erforderlich.

Das Suffix &quot;s&quot;gibt an, dass der Farbwert mit dem Eingabefarbraum (Quelle) verknüpft ist, der dem Pixeltyp des Farbwerts entspricht (definiert mit `attribute::IccProfileSrc*`). Wenn dieses Suffix nicht vorhanden ist, wird der Farbwert mit dem Ausgabefarbraum (Ziel) verknüpft (definiert mit `icc=` oder `attribute::IccProfile*`).

## Standard {#section-737082a7da544acca8092a48d88480e7}

Wenn ein Alpha-Wert nicht explizit angegeben wird, wird er als 255, 0xFF oder 100 % (vollständig undurchsichtig) angenommen.

## Beispiele {#section-4ac69026349949f8b595a6d4a9ce474d}

Einige Beispiele für gültige Farbspezifikatoren und den zugehörigen Pixeltyp, Farbwert, Alpha-Wert und Standardfarbraum:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Pixel-Typ</b> </th> 
   <th class="entry"> <b>Farbwert</b> </th> 
   <th class="entry"> <b>Alpha-Wert</b> </th> 
   <th class="entry"> <b>Standardfarbraum  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0.100.200.200 rs </p> </td> 
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
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100 S </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50.75 g </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grau </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94.11,50,33 k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22.23.24.25.26 KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Der mit `icc=` angegebene Ausgabefarbraum wird anstelle des Standardfarbraums angewendet, wenn der Pixeltyp einer Ausgabefarbung dem Pixeltyp des Ausgabebilds entspricht.
