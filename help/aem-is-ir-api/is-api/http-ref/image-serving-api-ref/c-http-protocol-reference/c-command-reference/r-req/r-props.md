---
description: Eigenschaften der Antwortdaten. Wertet die aktuelle Anfrage als Bildanforderung aus (req=img), gibt aber anstelle des Bildes vom Server ausgewählte Eigenschaften des Antwortbildes zurück.
solution: Experience Manager
title: props
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 5%

---

# props{#props}

Eigenschaften der Antwortdaten. Wertet die aktuelle Anfrage als Bildanforderung aus (req=img), gibt aber anstelle des Bildes vom Server ausgewählte Eigenschaften des Antwortbildes zurück.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p> </td> 
 </tr> 
</table>

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Unter [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) finden Sie eine Beschreibung der Antwortsyntax und des MIME-Typs der Antwort. Die HTTP-Antwort kann mit einer auf `attribute::NonImgExpiration` basierenden TTL zwischengespeichert werden.

Die folgenden Eigenschaften werden für &quot;/is/image“-Anfragen zurückgegeben:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beschreibung</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> Hexagon </p> </td> 
   <td> <p> Hintergrundfarbe (siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Höhe des Antwortbildes in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed-</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> True, wenn das ICC-Profil in das Antwortbild eingebettet ist. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile-</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Name/Beschreibung des Profils, das dem Antwortbild zugeordnet ist. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Antwortgröße in Pixeln, ohne HTTP-Kopfzeile; 0, wenn die Antwortbilddaten nicht zuvor vom Server zwischengespeichert wurden. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadCache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> 1 Wenn das Antwortbild einen Alphakanal enthält, andernfalls 0. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Antwortbildtyp, kann <span class="codeph"> CMYK-</span>, <span class="codeph"> RGB-</span> oder <span class="codeph"> BW-</span> (für Graustufenbilder) sein. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed-</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1 Wenn das Antwortbild Pfade einbettet, andernfalls 0. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes-</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> Druckauflösung (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> JPEG-Qualität. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> MIME-Typ für das Antwortbild. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Breite des Antwortbildes in Pixel. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1 Wenn das Antwortbild XMP-Daten einbettet, andernfalls 0. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Kennung der Bildversion. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> ID= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Kennung der Metadatenversion. (Siehe <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> ID= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

Die folgenden Eigenschaften werden für `/is/content` Anfragen zurückgegeben:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beschreibung</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p>Pfad der teilweise aufgelösten Datei. (Siehe <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Länge </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Größe der Objektdatei in Byte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-</span> </p> </td> 
   <td> <p> doppelt </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration </span> oder die standardmäßige Gültigkeitsdauer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified-</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Änderungsdatum/-uhrzeit (aus <span class="codeph"> statischen::TimeStamp-</span> oder der Objektdatei) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType-</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> static::UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
