---
description: Format des Antwortbilds.
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

Format des Antwortbilds.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Gibt das Bildkodierungsformat für an den Client gesendete Bilddaten und den entsprechenden Antwort-MIME-Typ für den HTTP-Antwortheader an. </p> <p> <span class="codeph"> jpeg </span>: verlustbehaftete JPEG </p> <p> <span class="codeph"> png </span>: verlustfreies PNG </p> <p> <span class="codeph"> png-alpha </span>: verlustfreies PNG mit Alphakanal </p> <p> <span class="codeph"> tif </span>: TIFF </p> <p> <span class="codeph"> tif-alpha </span>: TIFF mit Alphakanal </p> <p> <span class="codeph"> swf </span>: verlustbehaftetes JPEG eingebettet in eine Adobe-swf-Datei </p> <p> <span class="codeph"> pdf </span>: Bild eingebettet in PDF </p> <p> <span class="codeph"> gif </span>: GIF mit 2 bis 256 Farben </p> <p> <span class="codeph"> gif-alpha </span>: GIF mit 2 bis 255 Farben plus Key-Farbtransparenz </p> <p> <span class="codeph"> fxg </span>: FXG mit Variablen und angewendeter DOM-Manipulation </p> <p> <span class="codeph"> fxgraw </span>: Original auf dem Server gespeichertes FXG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | grau | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Kann verwendet werden, um den Ausgabefarbraum zu beeinflussen. </p> <p> <span class="codeph"> rgb </span>: RGB-Bilddaten zurückgeben </p> <p> <span class="codeph"> gray </span>: gibt Graustufen-Bilddaten zurück </p> <p> <span class="codeph"> cmyk </span>: CMYK-Bilddaten zurückgeben </p> </td> 
 </tr> 
</table>

`tiffCompression` ist nur zulässig, wenn tif, tif-alpha als Format angegeben ist. Die für diese Bildformate unterstützten Komprimierungsoptionen finden Sie in der folgenden Tabelle.

`qlt=` kann verwendet werden, um die JPEG-Kodierungsoptionen für die folgenden Formate festzulegen: JPEG, TIFF mit JPEG-Komprimierung. quantize= kann verwendet werden, wenn fmt=gif oder fmt=gif-alpha verwendet wird. Weitere Informationen finden Sie in den Befehlsbeschreibungen. Die anderen Formate verfügen nicht über konfigurierbare Optionen.

8 Bit pro Pixelkomponente werden für alle Formate und `pixelTypes[7]` zurückgegeben.

In der folgenden Tabelle sind die gültigen Kombinationen aus Format und `pixelType`, den entsprechenden HTTP-Antwort-MIME-Typen, aufgeführt.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Antwort-MIME-Typ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC-Profil einbetten </p> </th> 
   <th colname="col5" class="entry"> <p>Optionen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, grau, cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, grau </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, grau, cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, grau, cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, grau </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
