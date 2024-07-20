---
description: Eigenschaften des Bildkatalogs. Gibt allgemeine Attribute des im Anfragepfad angegebenen Bildkatalogs zurück.
solution: Experience Manager
title: Katalogproben
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 4%

---

# Katalogproben{#catalogprops}

Eigenschaften des Bildkatalogs. Gibt allgemeine Attribute des im Anfragepfad angegebenen Bildkatalogs zurück.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Um die standardmäßigen Katalogeigenschaften ( [!DNL default.ini]) abzurufen, lassen Sie die Katalog-ID weg. Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `attribute::NonImgExpiration` basiert.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Die folgenden Eigenschaftswerte werden zurückgegeben:

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Entsprechendes Katalogattribut</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph"> attribute::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::defaultExt</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> attribute::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> attribute::LastModified</span> oder, falls nicht vorhanden, die letzte Änderungszeit der Datei <span class="varname"> catalog</span><span class="filepath"> .ini</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> attribute::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> attribute::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> attribute::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::watermark</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> attribute::Watermark</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
