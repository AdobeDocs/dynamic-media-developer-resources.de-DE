---
description: Antwortbildformat. Gibt das Bildkodierungsformat für an den Client gesendete Bilddaten und den entsprechenden MIME-Typ der Antwort für den HTTP-Antwort-Header an.
seo-description: Antwortbildformat. Gibt das Bildkodierungsformat für an den Client gesendete Bilddaten und den entsprechenden MIME-Typ der Antwort für den HTTP-Antwort-Header an.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 4%

---


# fmt{#fmt}

Antwortbildformat. Gibt das Bildkodierungsformat für an den Client gesendete Bilddaten und den entsprechenden MIME-Typ der Antwort für den HTTP-Antwort-Header an.

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Format </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Verlustes JPEG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>Verlustes JPG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>Verlustfreies PNG-Format. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>Verlustfreies PNG mit Alpha-Kanal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFF mit Alpha-Kanal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Verlustbehaftetes JPEG, das in eine Macromedia-SWF-Datei eingebettet ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>Lossy JPEG und eine deflate-komprimierte Maske, die in eine Macromedia-SWF-Datei eingebettet ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>In PDF eingebettetes Bild. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>Unkomprimiertes binäres Encapsulated PostScript. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF mit 256 Farben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF mit 255 Farben plus Key-Farbtransparenz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Gibt RGB-Bilddaten zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>grau </p> </td> 
  <td class="stentry"> <p>Gibt Graustufen-Bilddaten zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>CMYK-Bilddaten zurückgeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>keine </p> </td> 
  <td class="stentry"> <p>Nicht komprimiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW (Lempel-Ziv-Welch) Komprimierung (verlustfrei). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>"Deflate"-Komprimierung (verlustfrei). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG-Komprimierung (verlustbehaftet). </p> </td> 
 </tr> 
</table>

*`pixelType`* Effekte, die eine Konvertierung des Ausgabefarbraums bewirken, wenn  `icc=` keine Angabe gemacht wird; das Profil für die Standardfarbe entsprechend  *`pixelType`* angewendet wird. Wenn das Farbmanagement deaktiviert ist, wird eine naive Konversion angewendet. *`pixelType`* wird ignoriert, wenn angegeben  `icc=` wird, was den Ausgabepipeltyp bestimmt.

*`compression`* ist nur zulässig, wenn tif, tif-alpha oder PDF als  *`format`*. Die für diese Bildformate unterstützten Komprimierungsoptionen finden Sie in der folgenden Tabelle.

`qlt-` legt die JPEG-Kodierungsoptionen für die folgenden Formate fest: JPEG, TIFF mit JPEG-Komprimierung, PDF mit JPEG-Komprimierung und SWF-Datei. Verwenden Sie `quantize=`, wenn `fmt=gif` oder `fmt=gif-alpha`. Weitere Informationen finden Sie in den Befehlsbeschreibungen. Die anderen Formate haben keine einstellbaren Optionen.

8 Bit pro Pixelkomponente werden für alle Formate und Pixeltypen zurückgegeben.

In der folgenden Tabelle werden die gültigen Kombinationen von *`format`* und *`pixelType`*, die entsprechenden HTTP-Antwort-MIME-Typen, ob ICC-Profil eingebettet werden können (siehe [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) und welche formatspezifischen Optionsbefehle angewendet werden können.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> Format </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Antwort-MIME-Typ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC-Profil einbetten </p> </th> 
   <th colname="col5" class="entry"> <p>Optionen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt  </span> </p> <p>( <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, <span class="varname"> tiffCompression </span> ist auf 'jpeg' eingestellt.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> <p>(Der Flash Player ignoriert eingebettete ICC-Profil.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> attribute::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt=  </span> </p> <p> ( <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, <span class="varname"> tiffCompression </span> ist auf 'jpeg' eingestellt.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau </p> <p>(Daten werden nach der Konvertierung in Grau oder RGB in eine Palette umgewandelt.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Gibt das Kodierungsformat für an den Client gesendete Antwortbilddaten und den entsprechenden MIME-Typ der Antwort für den HTTP-Antwort-Header an.

`png-alpha` gibt nicht verknüpftes Alpha zurück (d. h., Alpha multipliziert die Pixelwerte nicht), während  `tif-alpha`und  `swf-alpha` gibt verknüpftes Alpha zurück (d. h. die Alpha-Werte werden vormultipliziert mit den Alpha-Werten). Der Alpha-Kanal entspricht dem Umkehren der Vignettenhintergrundmaske für `req=img` und der Gruppen- oder Objektmaske für `req=object`. Um Alpha bei Verwendung einer verschachtelten IR-Anforderung anzuwenden, fügen Sie der eingebetteten IR-Anforderung und der Hauptanforderung `fmt=` mit dem entsprechenden Alpha-Dateiformat hinzu. Wenn ein CMYK- oder Graustufen-ICC-Profil mit `icc=` angegeben ist, werden keine Alpha-Daten zurückgegeben.

## Eigenschaften {#section-eb12a82c69d84622bcea153dd84d95b3}

Kann an beliebiger Stelle in der Anforderung auftreten.

## Standard {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* standardmäßig auf  `attribute::Format`und  *`tiffCompression`* standardmäßig auf  `attribute::TiffEncoding`. *`pixelType`* ist standardmäßig auf &quot; `rgb` wenn nicht angegeben  `icc=` ist&quot;festgelegt, andernfalls entspricht es dem Pixeltyp des angegebenen ICC-Profils.

## Verwandte Themen {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)  [ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)  [pathEmbed=,req=, σQuantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
