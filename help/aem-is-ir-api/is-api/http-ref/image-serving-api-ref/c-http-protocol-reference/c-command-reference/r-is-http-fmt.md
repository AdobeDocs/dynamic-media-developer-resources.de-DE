---
title: fmt
description: Format des Antwortbildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 2%

---

# fmt{#fmt}

Format des Antwortbildes.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - AVIF-Alpha | AVIF | EPS | F4M | gif-alpha | GIF | heic | JPEG | jpeg2000-alpha | JPEG2000 | jpegxr-alpha | JPEGXR | jpg | M3u8 | PDF | PJPEG | png-alpha | PNG | png8-alpha | png8 | swf-alpha | SWF | swf3-alpha | swf3 | TIF-Alpha | TIF | web-alpha | WebP

| *`format`* | Beschreibung |
|---|---|
| `avif-alpha` | Verlust- und verlustfreies AVIF mit Alphakanal. |
| `avif` | Verlustbehaftete und verlustfreie AVIF. |
| `eps` | Unkomprimierte binär verkapselte PostScript. |
| `f4m` | Flash-Streaming-Server-Manifestformat. |
| `gif-alpha` | GIF mit 2 bis 255 Farben plus Key-Color-Transparenz. |
| `gif` | GIF mit 2 bis 256 Farben. |
| `heic` | Verlustfreie HEIC. Dieses Format wird standardmäßig vom Browser heruntergeladen, wenn es nicht unterstützt wird. |
| `jpeg` | Verlustbehaftetes JPEG. |
| `jpeg2000-alpha` | Verlustbehaftete und verlustfreie JPEG 2000 mit Alphakanal. |
| `jpeg2000` | Verlustbehaftete und verlustfreie JPEG 2000. |
| `jpegxr-alpha` | Verlustbehaftete und verlustfreie JPEG XR mit Alphakanal. |
| `jpegxr` | Verlustbehaftetes und verlustfreies JPEG XR. |
| `jpg` | Verlustbehaftete JPG. |
| `m3u8` | Apple-Streaming-Server-Manifestformat. |
| `pdf` | Bild eingebettet in PDF. |
| `pjpeg` | Progressives JPEG. |
| `png-alpha` | 24-Bit-verlustfreies PNG mit Alphakanal. |
| `png` | 24-Bit-verlustfreies PNG. |
| `png8-alpha` | 8-Bit-verlustfreies PNG mit Alphakanal. |
| `png8` | 8-Bit-verlustfreies PNG. |
| `swf-alpha` | Verlustbehaftetes JPEG und eine Deflate-komprimierte Maske, eingebettet in eine Adobe AS2 SWF-Datei. |
| `swf` | Verlorene JPEG eingebettet in eine Adobe AS2 SWF-Datei. |
| `swf3-alpha` | Verlustbehaftetes JPEG und eine Deflate-komprimierte Maske, eingebettet in eine Adobe AS3 SWF-Datei. **Hinweis:** swf- und swf-alpha-Formate eignen sich am besten für ActionScript 2-Anwendungen (Flash Player 8 und früher). Die Formate swf3 und swf3-alpha werden für ActionScript3-Anwendungen (Flash Player 9 und höher) empfohlen. |
| `swf3` | Verlorene JPEG eingebettet in eine Adobe AS3 SWF-Datei. |
| `tif-alpha` | TIFF mit Alphakanal. |
| `tif` | TIFF. |
| `webp-alpha` | Verlorenes und verlustfreies WebP mit Alphakanal. |
| `webp` | Verlust- und verlustfreies WebP. |

*`pixelType`* - rgb | grau | CMYK

| *`pixelType`* | Beschreibung |
|---|---|
| `cmyk` | Gibt CMYK-Bilddaten zurück. |
| `gray` | Gibt Bilddaten mit Graustufen zurück. |
| `rgb` | Gibt RGB-Bilddaten zurück. |

*`compression`* - JPEG | verlustreich | verlustfrei | Gesetz | Keine | PLZ

| *`compression`* | Beschreibung |
|---|---|
| `jpeg` | JPEG-Komprimierung (verlustbehaftet) |
| `lossy` | JPEG 2000 und JPEG XR-Komprimierung (verlustbehaftet) und WebP. |
| `lossless` | HEIC, JPEG 2000 und JPEG XR-Komprimierung (verlustfrei) und WebP. |
| `lzw` | LZW (Lempel-Ziv-Welch) Kompression (verlustfrei). |
| `none` | Unkomprimiert. |
| `zip` | Kompression „Deflate“ (verlustfrei). |

* *`format`* gibt das Bildcodierungsformat für die an den Client gesendeten Bilddaten sowie den entsprechenden Antwort-MIME-Typ für den HTTP-Antwort-Header an.
* *`pixelType`* kann verwendet werden, um die Konvertierung des Ausgabefarbraums zu bewirken, wenn `icc=` nicht angegeben ist.

  Das Standardfarbprofil, das *`pixelType`* entspricht, wird angewendet. Wenn das Farbmanagement deaktiviert ist, wird eine naive Konvertierung angewendet. *`pixelType`* wird ignoriert, wenn `icc=` angegeben wird, was den Pixel-Ausgabetyp bestimmt.

* *`compression`* ist nur zulässig, wenn `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr` oder `jpegxr-alpha` als *`format`* angegeben ist. In der folgenden Tabelle finden Sie die Komprimierungsoptionen, die für diese Bildformate unterstützt werden.

Sie können `qlt=` verwenden, um die JPEG-Kodierungsoptionen für die folgenden Formate festzulegen: JPEG, TIFF mit JPEG-Komprimierung, PDF mit JPEG-Komprimierung und SWF. WebP, JPEG 2000 und JPEG XR verwenden ebenfalls `qlt=`, aber die Werte führen zu unterschiedlichen Qualitäten für die verschiedenen Formate. Verwenden Sie `quantize=`, wenn `fmt=gif` oder `fmt=gif-alpha`. Einzelheiten finden Sie in den Befehlsbeschreibungen. Für die anderen Formate gibt es keine einstellbaren Optionen.

Für alle *`formats`* und *`pixelTypes`* werden 8 Bit pro Pixelkomponente zurückgegeben (8 Bit pro Pixel für GIF).

In der folgenden Tabelle sind die gültigen Kombinationen von *`format`* und *`pixelType`*, die entsprechenden HTTP-Antwort-MIME-Typen, die Frage, ob ICC-Profile eingebettet werden können (siehe [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)), und die möglichen formatspezifischen Optionen aufgeführt.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> Format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Antwort MIME-Typ</b> </th> 
   <th class="entry"> <b>ICC-Profil </b> </th> 
   <th class="entry"> <b> Optionen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> AVIF, AVIF-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> Komprimierung </span> </span> ( <span class="codeph"> verlustbehaftetes </span>, <span class="codeph"> verlustfreie </span>) </p> <p> <span class="codeph"> qlt= </span> wird für <span class="codeph"> verlustfreie </span> ignoriert. </p> <p>Da es kein Konzept für die Neuberechnung der Chrominanz mit dem WebP-Format gibt, wird bei Verwendung eines zweiten Werts mit <span class="codeph"> qlt-</span> (z. B. <span class="codeph"> qlt=80,1 </span>) der zweite Wert ( <span class="codeph"> 1 </span>) ignoriert. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> EPS </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt;-</span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> GIF, GIF-Alpha </p> </td> 
   <td colname="col2"> <p>RGB, grau </p> <p>Die Daten werden nach der Konvertierung in Grau oder RGB in eine Palette umgewandelt. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>RGB, grau </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> Komprimierung </span> </span> ( <span class="codeph"> verlustbehaftetes </span>, <span class="codeph"> verlustfreie </span>) </p> <p> <span class="codeph"> qlt= </span> wird für <span class="codeph"> verlustfreie </span> ignoriert. </p> <p>Da es kein Konzept für die Neuberechnung der Chrominanz mit dem WebP-Format gibt, wird bei Verwendung eines zweiten Werts mit <span class="codeph"> qlt-</span> (z. B. <span class="codeph"> qlt=80,1 </span>) der zweite Wert ( <span class="codeph"> 1 </span>) ignoriert. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt;-</span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Der Parameter <span class="codeph"> pscan= </span> gilt nur für das PJPEG-Format. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> Komprimierung </span> </span> ( <span class="codeph"> verlustbehaftetes </span>, <span class="codeph"> verlustfreie </span>) </p> <p> <span class="codeph"> qlt= </span> wird für <span class="codeph"> verlustfreie </span> ignoriert. </p> <p>Da es kein Konzept für die Neuberechnung der Chrominanz mit dem WebP-Format gibt, wird bei Verwendung eines zweiten Werts mit <span class="codeph"> qlt-</span> (z. B. <span class="codeph"> qlt=80,1 </span>) der zweite Wert ( <span class="codeph"> 1 </span>) ignoriert. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> Komprimierung </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, <span class="codeph"> <span class="varname"> Komprimierung </span> </span> ist auf <span class="codeph"> JPEG </span> eingestellt. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>RGB, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>RGB, grau </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nein </p> <p> <p>Hinweis: Die Adobe-Flash Player ignoriert eingebettete ICC-Profile. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> Attribut::TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> TIF, TIF-Alpha </p> </td> 
   <td colname="col2"> <p>RGB, Grau, CMYK </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt;-</span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> Komprimierung </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>Nur „tiff“; „tiff-alpha“ unterstützt keine JPEG-Komprimierung. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> wird ignoriert, es sei denn, <span class="varname"> Komprimierungs-</span> ist auf <span class="codeph"> JPEG-</span> festgelegt. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>WebP, WebP-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Nein </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> Komprimierung </span> </span> ( <span class="codeph"> verlustbehaftetes </span>, <span class="codeph"> verlustfreie </span>) </p> <p> <span class="codeph"> qlt= </span> wird für <span class="codeph"> verlustfreie </span> ignoriert. </p> <p>Da es kein Konzept für die Neuberechnung der Chrominanz mit dem WebP-Format gibt, wird bei Verwendung eines zweiten Werts mit <span class="codeph"> qlt-</span> (z. B. <span class="codeph"> qlt=80,1 </span>) der zweite Wert ( <span class="codeph"> 1 </span>) ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Anforderungsattribut. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet, wenn `req=img` (Standard) oder `req=mask`; andernfalls wird ignoriert.

*`type`* wird ignoriert, wenn `iccProfile=` angegeben ist.

## Standard {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, bei dem die *`defaultType`* wie folgt behandelt wird: Wenn `icc=` angegeben ist, entspricht *`defaultType`* dem Pixeltyp des angegebenen ICC-Profils. Wenn `icc=` nicht angegeben ist, wird *`defaultType`* bei `req=mask` `gray`, andernfalls `rgb`.

## Beispiele {#section-b93222e652df404a84c69025247f07df}

**Anfordern eines kleinen Vorschaubilds in niedriger Qualität im JPEG-Format (Standard):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Fordern Sie dasselbe Bild an, das in Graustufen konvertiert wurde:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Fordern Sie dasselbe Bild in einem verlustfreien Format mit Alphakanal und hoher Auflösung an:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Anfordern des Alphakanals für dasselbe Bild wie ein Graustufen-TIFF-Bild:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Konvertieren Sie dasselbe Bild mithilfe der standardmäßigen ICC-Profile in CMYK:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Konvertieren Sie dasselbe Bild mithilfe eines anderen ICC-Profils in CMYK und betten Sie das Profil in das TIFF-Bild ein:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Stellen Sie dieses Bild als TIF-Datei mit JPEG-Komprimierung ohne Pixeltypkonvertierung bereit:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Konvertieren Sie das Bild in eine zweifarbige GIF mit Schlüsselfarbtransparenz und erzwingen Sie Farben in Schwarzweiß:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**verlustbehaftet mit einer Qualitätseinstellung von 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Verlustfrei mit Alpha:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**verlustbehaftet mit einer Qualitätseinstellung von 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Verlustfrei mit Alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**verlustbehaftet mit einer Qualitätseinstellung von 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Verlustfrei mit Alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Verwandte Themen {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
