---
title: fmt
description: Bildformat der Antwort. Gibt das Bildcodierungsformat für an den Client gesendete Bilddaten sowie den entsprechenden Antwort-MIME-Typ für den HTTP-Antwort-Header an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 4%

---

# fmt {#fmt}

Bildformat der Antwort. Gibt das Bildcodierungsformat für an den Client gesendete Bilddaten sowie den entsprechenden Antwort-MIME-Typ für den HTTP-Antwort-Header an.

` fmt= *`format`*[,[ *`pixelType`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>JPEG </p> </td> 
  <td class="stentry"> <p>Verlustbehaftetes JPEG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>Verlustbehaftete JPG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>Verlustfreies PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>Verlustfreies PNG mit Alphakanal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>TIF </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>TIF-Alpha </p> </td> 
  <td class="stentry"> <p>TIFF mit Alphakanal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Verlorene JPEG in eine Macromedia SWF-Datei eingebettet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>Verlustbehaftetes JPEG und eine in eine Macromedia SWF-Datei eingebettete Deflate-komprimierte Maske. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Bild eingebettet in PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>EPS </p> </td> 
  <td class="stentry"> <p>Unkomprimierte binär verkapselte PostScript. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF mit 256 Farben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF mit 255 Farben plus Key-Color-Transparenz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType-</span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Gibt RGB-Bilddaten zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>grau </p> </td> 
  <td class="stentry"> <p>Gibt Bilddaten mit Graustufen zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>CMYK </p> </td> 
  <td class="stentry"> <p>Gibt CMYK-Bilddaten zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>keine </p> </td> 
  <td class="stentry"> <p>Unkomprimiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>Gesetz </p> </td> 
  <td class="stentry"> <p>LZW (Lempel-Ziv-Welch) Kompression (verlustfrei). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Kompression „Deflate“ (verlustfrei). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>JPEG </p> </td> 
  <td class="stentry"> <p>JPEG-Komprimierung (verlustbehaftet) </p> </td> 
 </tr> 
</table>

*`pixelType`* Bewirkt die Konvertierung des Ausgabefarbraums, wenn `icc=` nicht angegeben ist. Das Standardfarbprofil, das *`pixelType`* entspricht, wird angewendet. Wenn das Farbmanagement deaktiviert ist, wird eine naive Konvertierung angewendet. *`pixelType`* Wird ignoriert, wenn `icc=` angegeben wird. Dies bestimmt den Pixel-Typ der Ausgabe.

*`compression`* Nur zulässig, wenn tif, tif-alpha oder PDF als *`format`* angegeben ist. In der folgenden Tabelle finden Sie die Komprimierungsoptionen, die für diese Bildformate unterstützt werden.

`qlt-` Legt die JPEG-Kodierungsoptionen für die folgenden Formate fest: JPEG, TIFF mit JPEG-Komprimierung, PDF mit JPEG-Komprimierung und SWF-Datei. Verwenden Sie `quantize=`, wenn `fmt=gif` oder `fmt=gif-alpha`. Einzelheiten finden Sie in den Befehlsbeschreibungen. Für die anderen Formate gibt es keine einstellbaren Optionen.

Für alle Formate und Pixeltypen werden acht Bit pro Pixelkomponente zurückgegeben.

In der folgenden Tabelle sind die gültigen Kombinationen von *`format`* und *`pixelType`*, die entsprechenden HTTP-Antwort-MIME-Typen, die Frage, ob ICC-Profile eingebettet werden können (siehe [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) und welche formatspezifischen Optionsbefehle angewendet werden können, aufgeführt.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname">-</span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType-</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Antwort-MIME-Typ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC-Profil einbetten </p> </th> 
   <th colname="col5" class="entry"> <p>Optionen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt;-</span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>RGB, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>TIF, TIF-Alpha </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt;-</span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt </span> </p> <p>( <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, <span class="varname"> tiffCompression-</span> ist auf „jpeg“ festgelegt.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SWF, SWF-Alpha </p> </td> 
   <td colname="col2"> <p>RGB, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> <p>(Die Flash Player ignoriert eingebettete ICC-Profile.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> Attribut::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, <span class="varname"> tiffCompression-</span> ist auf „jpeg“ festgelegt.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>EPS </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt;-</span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>GIF, GIF-Alpha </p> </td> 
   <td colname="col2"> <p>RGB, grau </p> <p>(Die Daten werden nach der Konvertierung in Grau oder RGB in eine Palette umgewandelt.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Gibt das Kodierungsformat für die an den Client gesendeten Antwortbilddaten und den entsprechenden Antwort-MIME-Typ für die HTTP-Antwortkopfzeile an.

`png-alpha` Gibt nicht zugeordnete Alpha-Werte zurück (d. h. Alpha multipliziert die Pixelwerte nicht vorab), während `tif-alpha` und `swf-alpha` zugeordnete Alpha-Werte zurückgeben (d. h. die Alpha-Werte werden vorab mit den Alpha-Werten multipliziert). Der Alphakanal entspricht dem Inversen der Hintergrundmaske der Vignette für `req=img` und der Gruppen- oder Objektmaske, falls `req=object` vorhanden ist. Um Alpha bei Verwendung einer verschachtelten IR-Anfrage anzuwenden, fügen Sie der eingebetteten IR-Anfrage und der Hauptanfrage `fmt=` mit dem entsprechenden Alpha-Dateiformat hinzu. Wenn ein CMYK- oder Graustufen-ICC-Profil mit `icc=` angegeben wird, werden keine Alpha-Daten zurückgegeben.

## Eigenschaften {#section-eb12a82c69d84622bcea153dd84d95b3}

Kann überall in der Anfrage auftreten.

## Standard {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* Standardwert ist `attribute::Format`und *`tiffCompression`* Standardwert ist `attribute::TiffEncoding`. *`pixelType`* ist standardmäßig `rgb`, wenn `icc=` nicht angegeben ist. Andernfalls entspricht dies dem Pixeltyp des angegebenen ICC-Profils.

## Verwandte Themen {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb), [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
