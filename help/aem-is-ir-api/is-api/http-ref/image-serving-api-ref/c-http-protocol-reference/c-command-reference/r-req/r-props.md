---
description: Eigenschaften von Antwortdaten. Wertet die aktuelle Anforderung so aus, als wäre es eine Bildanforderung (req=img), gibt der Server jedoch anstelle der Bildausgabe ausgewählte Eigenschaften des Antwortbilds zurück.
seo-description: Eigenschaften von Antwortdaten. Wertet die aktuelle Anforderung so aus, als wäre es eine Bildanforderung (req=img), gibt der Server jedoch anstelle der Bildausgabe ausgewählte Eigenschaften des Antwortbilds zurück.
seo-title: props
solution: Experience Manager
title: props
topic: Scene7 Image Serving - Image Rendering API
uuid: b9325654-81d6-4f00-bf0a-36650bea6b8d
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 8%

---


# props{#props}

Eigenschaften von Antwortdaten. Wertet die aktuelle Anforderung so aus, als wäre es eine Bildanforderung (req=img), gibt der Server jedoch anstelle der Bildausgabe ausgewählte Eigenschaften des Antwortbilds zurück.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p> </td> 
 </tr> 
</table>

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.

Eine Beschreibung der Antwortsyntax und des Antworttyps finden Sie unter [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9). Die HTTP-Antwort kann mit einer TTL, die auf `attribute::NonImgExpiration` basiert, zwischengespeichert werden.

Die folgenden Eigenschaften werden für /is/image-Anforderungen zurückgegeben:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beschreibung</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> Hintergrundfarbe (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Bildhöhe in Pixel beantworten </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> True, wenn das ICC-Profil in das Antwortbild eingebettet ist. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Name/Beschreibung des Profils, das mit dem Antwortbild verknüpft ist. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Antwortgröße in Pixeln ohne HTTP-Kopfzeile; 0, wenn die Antwortbilddaten zuvor nicht vom Server zwischengespeichert wurden. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1, wenn das Antwortbild einen Alpha-Kanal enthält, andernfalls 0. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Reply image type, may be <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> oder <span class="codeph"> BW </span> (for gray-scale images). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das Antwortbild Pfade einbettet, andernfalls 0. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> Druckauflösung (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> JPEG-Qualität. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Mime-Typ für das Antwortbild. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Replizieren Sie die Bildbreite in Pixel. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das Antwortbild xmp-Daten einbettet, andernfalls 0. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Identifikator der Bildversion. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Metadaten-Versionskennung. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

Für `/is/content`-Anforderungen werden die folgenden Eigenschaften zurückgegeben:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beschreibung</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Pfade </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p>Teilweise aufgelöster Dateipfad. (Siehe <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Objektdateigröße in Byte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Ablauf </span> </p> </td> 
   <td> <p> doppelt </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration  </span> oder die standardmäßige "live"-Zeit </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Änderungsdatum/-zeit (von <span class="codeph"> static::TimeStamp </span> oder der Objektdatei) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> static::UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

