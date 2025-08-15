---
description: Format des Antwortbildes.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# fmt{#fmt}

Format des Antwortbildes.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> JPEG | PNG | png-alpha | TIF | TIF-Alpha | SWF | PDF | GIF | gif-alpha | FXG | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Gibt das Bildcodierungsformat für Bilddaten an, die an den Client gesendet werden, und den entsprechenden Antwort-MIME-Typ für den HTTP-Antwort-Header an. </p> <p> <span class="codeph"> JPEG-</span>: Verlorene JPEG </p> <p> <span class="codeph"> PNG </span>: verlustfreies PNG </p> <p> <span class="codeph"> png-alpha </span>: verlustfreies PNG mit Alphakanal </p> <p> <span class="codeph"> TIF-</span>: TIFF </p> <p> <span class="codeph"> TIF-Alpha-</span>: TIFF mit Alphakanal </p> <p> <span class="codeph"> SWF-</span>: verlustbehaftetes JPEG, das in eine Adobe-SWF-Datei eingebettet ist </p> <p> <span class="codeph"> PDF </span>: Bild eingebettet in PDF </p> <p> <span class="codeph"> GIF </span>: GIF mit 2 bis 256 Farben </p> <p> <span class="codeph"> GIF-Alpha </span>: GIF mit 2 bis 255 Farben plus Schlüsselfarbtransparenz </p> <p> <span class="codeph"> fxg </span>: FXG mit Variablen und angewendeter DOM-Manipulation </p> <p> <span class="codeph"> fxgraw </span>: Original-FXG auf dem Server gespeichert </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> RGB | grau | CMYK</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Kann verwendet werden, um den Ausgabefarbraum zu beeinflussen. </p> <p> RGB-<span class="codeph"> </span>: RGB-Bilddaten zurückgeben </p> <p> <span class="codeph">-</span>: Gibt Bilddaten mit Graustufen zurück </p> <p> <span class="codeph"> CMYK-</span>: Gibt CMYK-Bilddaten zurück </p> </td> 
 </tr> 
</table>

`tiffCompression` ist nur zulässig, wenn TIF, TIF-Alpha als Format angegeben ist. In der folgenden Tabelle finden Sie die Komprimierungsoptionen, die für diese Bildformate unterstützt werden.

`qlt=` können verwendet werden, um die JPEG-Kodierungsoptionen für die folgenden Formate festzulegen: JPEG, TIFF mit JPEG-Komprimierung. quantize= kann verwendet werden, wenn fmt=gif oder fmt=gif-alpha. Einzelheiten finden Sie in den Befehlsbeschreibungen. Für die anderen Formate gibt es keine einstellbaren Optionen.

Für alle Formate und `pixelTypes[7]` werden 8 Bit pro Pixelkomponente zurückgegeben.

In der folgenden Tabelle sind die gültigen Kombinationen aus Format und `pixelType` sowie die entsprechenden HTTP-Antwort-MIME-Typen aufgeführt.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> Format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Antwort-MIME-Typ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC-Profil einbetten </p> </th> 
   <th colname="col5" class="entry"> <p>Optionen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>JPEG </p> </td> 
   <td> <p>RGB, Grau, CMYK </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>RGB, grau </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>TIF, TIF-Alpha </p> </td> 
   <td> <p>RGB, Grau, CMYK </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( keine | Gesetz | PLZ | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>SWF, SWF-Alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>RGB, Grau, CMYK </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>GIF, GIF-Alpha </p> </td> 
   <td> <p>RGB, grau </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
