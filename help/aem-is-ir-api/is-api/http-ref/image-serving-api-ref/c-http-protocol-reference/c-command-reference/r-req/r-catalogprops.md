---
description: Bildkatalogeigenschaften. Gibt allgemeine Attribute des im Anfragepfad angegebenen Bildkatalogs zurück.
solution: Experience Manager
title: catalogProps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 4%

---

# catalogProps{#catalogprops}

Bildkatalogeigenschaften. Gibt allgemeine Attribute des im Anfragepfad angegebenen Bildkatalogs zurück.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Um die Standardkatalogeigenschaften abzurufen ([!DNL default.ini]), lassen Sie die Katalog-ID weg. Die HTTP-Antwort kann basierend auf `attribute::NonImgExpiration` mit der TTL zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Die folgenden Eigenschaftswerte werden zurückgegeben:

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> entsprechende Katalogattribut</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> Hexagon </p> </td> 
   <td> <p> <span class="codeph">::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::defaultExt</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph">::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int, int </p> </td> 
   <td> <p> <span class="codeph">::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int, int </p> </td> 
   <td> <p> <span class="codeph">::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.expiration</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">::Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">-Attribut::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> Attribut::LastModified</span> oder, falls nicht vorhanden, die letzte Änderungszeit der <span class="varname"> Katalog</span><span class="filepath"> .ini</span> Datei </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph">::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int, int </p> </td> 
   <td> <p> <span class="codeph">::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph">-Attribut::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph">::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> <span class="codeph">-Attribut::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> Hexagon </p> </td> 
   <td> <p> <span class="codeph">::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> <span class="codeph">::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> <span class="codeph">::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> <span class="codeph">::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::watermark</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph">::Watermark</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
