---
description: Antwortbildformat.
seo-description: Antwortbildformat.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 5%

---


# fmt{#fmt}

Antwortbildformat.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alpha | swf | swf-alpha | swf3 | swf3-alpha | eps | gif | gif-alpha | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alpha | jpegxr | jpegxr-alpha

| *`format`* | Beschreibung |
|---|---| 
| `jpeg` | Lossy JPEG |
| `jpg` | Lossy JPG |
| `pjpeg` | Progressives JPEG |
| `png` | 24-Bit-verlustfreies PNG-Format |
| `png8` | 8-Bit-verlustfreies PNG-Format |
| `png-alpha` | 24-Bit-verlustfreies PNG-Format mit Alpha-Kanal |
| `png8-alpha` | 8-Bit-verlustfreies PNG-Format mit Alpha-Kanal |
| `tif` | TIFF |
| `tif-alpha` | TIFF mit Alpha-Kanal |
| `pdf` | In PDF eingebettetes Bild |
| `eps` | Unkomprimiertes binäres Encapsulated PostScript |
| `gif` | GIF mit 2 bis 256 Farben |
| `gif-alpha` | GIF-Format mit 2 bis 255 Farben plus Key-Farbtransparenz |
| `swf` | Verlustfreies JPEG, das in eine SWF-Datei der Adobe AS2 eingebettet ist |
| `swf-alpha` | Verlustes JPEG und eine deflate-komprimierte Maske, die in eine Adobe AS2 SWF-Datei eingebettet ist |
| `swf3` | Verlustfreies JPEG, eingebettet in eine Adobe AS3-SWF-Datei |
| `swf3-alpha` | Verlustfreies JPEG und eine deflate-komprimierte Maske, die in eine Adobe AS3-SWF-Datei eingebettet ist. **Hinweis**: Die Formate swf und swf-alpha eignen sich am besten für ActionScript 2-Anwendungen (Flash Player 8 und früher). swf3 und swf3-alpha werden für ActionScript3-Anwendungen empfohlen (Flash Player 9 und höher). |
| `m3u8` | Manifestformat von Apple Streaming Server |
| `f4m` | Manifestformat &quot;Flash Streaming Server&quot; |
| `webp` | Verlustfreies und verlustfreies WebP |
| `webp-alpha` | Verlustfreies und verlustfreies WebP mit Alpha-Kanal |
| `jpeg2000` | Verlustfreies und verlustfreies JPEG 2000 |
| `jpeg2000-alpha` | Verlustfreies und verlustfreies JPEG 2000 mit Alpha-Kanal |
| `jpegxr` | Verlustfreies und verlustfreies JPEG XR |
| `jpegxr-alpha` | Verlustfreies und verlustfreies JPEG XR mit Alpha-Kanal |


| *`pixelType`* — rgb | grau | cmyk |
| *`pixelType`* | Beschreibung |
|---|---|
| `rgb` | Gibt RGB-Bilddaten zurück. |
| `gray` | Gibt Graustufen-Bilddaten zurück. |
| `cmyk` | CMYK-Bilddaten zurückgeben. |

| *`compression`* — none | lzw | zip | jpeg | verlustbehaftet | verlustfrei |
| *`compression`* | Beschreibung |
|---|---|
| `none` | Nicht komprimiert |
| `lzw` | LZW-Komprimierung (Lempel-Ziv-Welch) (verlustfrei) |
| `zip` | &quot;Deflate&quot;-Komprimierung (verlustfrei) |
| `jpeg` | JPEG-Komprimierung (verlustbehaftet) |
| `lossy` | WebP-, JPEG 2000- und JPEG XR-Komprimierung (verlustbehaftet) |
| `lossless` | WebP-, JPEG 2000- und JPEG XR-Komprimierung (verlustfrei) |

* *`format`* gibt das Bildkodierungsformat für an den Client gesendete Bilddaten und den entsprechenden MIME-Typ der Antwort für den HTTP-Antwort-Header an.
* *`pixelType`* kann verwendet werden, um die Konvertierung des Ausgabefarbraums auszuführen, wenn nicht angegeben `icc=` ist.

   Es *`pixelType`* wird das Profil für die Standardfarbe entsprechend angewendet. Wenn das Farbmanagement deaktiviert ist, wird eine naive Konversion angewendet. *`pixelType`* wird ignoriert, wenn angegeben `icc=` wird, was den Ausgabepipeltyp bestimmt.

* *`compression`* ist nur zulässig, wenn `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`oder `jpegxr-alpha` als *`format`*. Die für diese Bildformate unterstützten Komprimierungsoptionen finden Sie in der folgenden Tabelle.

Sie können die JPEG-Kodierungsoptionen `qlt=` für folgende Formate festlegen: JPEG, TIFF mit JPEG-Komprimierung, PDF mit JPEG-Komprimierung und SWF. WebP, JPEG 2000 und JPEG XR verwenden ebenfalls, `qlt=` aber die Werte führen zu unterschiedlichen Qualitäten für die verschiedenen Formate. Verwenden Sie `quantize=` wenn `fmt=gif` oder `fmt=gif-alpha`. Weitere Informationen finden Sie in den Befehlsbeschreibungen. Die anderen Formate haben keine einstellbaren Optionen.

8 Bit pro Pixelkomponente werden für alle *`formats`* und *`pixelTypes`* (8 Bit pro Pixel für GIF) zurückgegeben.

In der folgenden Tabelle werden die gültigen Kombinationen aus *`format`*und *`pixelType`*, die entsprechenden HTTP-Antwort-MIME-Typen, ob ICC-Profil eingebettet werden können (siehe [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) und welche formatspezifischen Optionen angewendet werden können.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Antwort-MIME-Typ</b> </th> 
   <th class="entry"> <b>ICC-Profil einbetten</b> </th> 
   <th class="entry"> <b> Optionen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Der Parameter <span class="codeph"> pscan= </span> gilt nur für das pjpeg-Format. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>nur 'tiff'; 'tiff-alpha' unterstützt keine JPEG-Komprimierung. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, die <span class="varname"> Komprimierung </span> ist auf <span class="codeph"> jpeg eingestellt </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> <p> <p>Hinweis:  Der Flash Player Adobe ignoriert eingebettete ICC-Profil. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, die <span class="codeph"><span class="varname"> Komprimierung </span> ist auf </span> jpeg eingestellt <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, grau, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grau </p> <p>Daten werden nach der Konvertierung in Grau oder RGB in eine Palette umgewandelt. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> Komprimierung </span> ( </span> verlustbehaftet <span class="codeph"> , </span>verlustfrei <span class="codeph"> </span>) </p> <p> <span class="codeph"> qlt= </span> wird für <span class="codeph"> verlustfrei ignoriert </span>. </p> <p>Da es kein Konzept für die Chrominanz-Neuberechnung mit dem WebP-Format gibt, wird bei Verwendung eines zweiten Werts mit <span class="codeph"> qlt </span> (z. B. <span class="codeph"> qlt=80,1 </span>) der zweite Wert ( <span class="codeph"> 1 </span>) ignoriert. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grau </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p>Wie oben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p>Wie oben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung, wenn `req=img` (Standard) oder `req=mask`; andernfalls ignoriert.

*`type`* wird ignoriert, wenn angegeben `iccProfile=` wird.

## Standard {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, wobei die Variable wie folgt verarbeitet *`defaultType`* wird: Wenn `icc=` angegeben, *`defaultType`* entspricht dem Pixeltyp des angegebenen ICC-Profils. Wenn `icc=` nicht angegeben, ist *`defaultType`* , `gray` wenn `req=mask`, andernfalls ist es `rgb`.

## Beispiele {#section-b93222e652df404a84c69025247f07df}

**Fordern Sie ein kleines Bild mit niedriger Vorschau im JPEG-Format (Standard) an:**

` http:// *`Server`*/myRootId/myImageId?qlt=60&wid=200`

**Erfordert dasselbe Bild, das in Graustufen konvertiert wurde:**

` http:// *`Server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Fordern Sie dasselbe Bild in einem verlustfreien Format mit Alpha-Kanal und hoher Auflösung an:**

` http:// *`Server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Fordern Sie den Alpha-Kanal für dasselbe Bild wie ein Graustufenbild-TIFF-Bild an:**

` http:// *`Server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Konvertieren Sie dasselbe Bild mit den standardmäßigen ICC-Profilen in cmyk:**

` http:// *`Server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Konvertieren Sie dasselbe Bild mit einem anderen ICC-Profil in cmyk und betten Sie das Profil in das TIFF-Bild ein:**

` http:// *`Server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Stellen Sie dieses Bild als TIF-Datei mit JPEG-Komprimierung ohne Konvertierung des Pixeltyps bereit:**

` http:// *`Server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Konvertieren Sie das Bild in ein bitonales GIF mit Key-Farbtransparenz und erzwingen Sie Farben in Schwarzweiß:**

` http:// *`Server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Verlust bei einer Qualitätseinstellung von 80:**

` http:// *`Server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Verlustfrei mit Alpha:**

` http:// *`Server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Verlust bei einer Qualitätseinstellung von 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Verlustfrei mit Alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Verlust bei einer Qualitätseinstellung von 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Verlustfrei mit Alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Verwandte Themen {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)pathEmbed=,pscan.
