---
description: Source-Bildeigenschaften. Gibt die ausgewählten Eigenschaften der im URL-Pfad angegebenen Bilddatei oder des Katalogeintrags zurück.
solution: Experience Manager
title: imageProps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 4%

---

# imageProps{#imageprops}

Source-Bildeigenschaften. Gibt die ausgewählten Eigenschaften der im URL-Pfad angegebenen Bilddatei oder des Katalogeintrags zurück.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Die HTTP-Antwort kann basierend auf `attribute::NonImgExpiration` mit der TTL zwischengespeichert werden.

Andere Befehle in der Anfragezeichenfolge werden ignoriert.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Die folgenden Eigenschaften werden zurückgegeben:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschaft</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beschreibung</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int, int </p> </td> 
   <td> <p> <span class="codeph">::Anchor</span> oder der standardmäßige Ankerpunkt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> doppelt </p> </td> 
   <td> <p> <span class="codeph">::Expiration</span> oder die Standardlebensdauer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Bildhöhe in voller Auflösung in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Name/Beschreibung des mit diesem Bild verknüpften Profils </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bild <span class="codeph">. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1 , wenn das zugehörige Profil in das Bild eingebettet ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded FotoshopPaths</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1 Wenn das Bild Photoshop-Pfaddaten enthält </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bild <span class="codeph">. embeddedXmpData</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1 Wenn das Bild XMP-Daten enthält </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> 0 für keine Maske, 1 für vormultipliziertes Alpha, 2 für nicht vormultipliziertes Alpha und 3 für ein separates Maskenbild </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph">::Modifier</span> oder leer, wenn kein Katalogeintrag vorhanden ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bild <span class="codeph">. photoshopPathNames</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Kommagetrennte Liste der Namen aller mit diesem Bild verknüpften Photoshop-Pfade </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Bildtyp, kann „CMYK“, "RGB" oder „BW“ (für Graustufenbilder) sein </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph">::PostModifier</span> oder leer, wenn kein Katalogeintrag vorhanden ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> Standardmäßige Druckauflösung in Pixel/Zoll </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">::Resolution </span> die Standardobjektauflösung </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p>Änderungsdatum/-uhrzeit (aus <span class="codeph"> Katalog::TimeStamp</span> oder der Bilddatei) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph">::ThumbRes</span> oder die Standardauflösung für Miniaturen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> Aufzählung </p> </td> 
   <td> <p> <span class="codeph">::ThumbType</span> oder der Standardtyp für Miniaturen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Bildbreite in voller Auflösung in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Katalog-ID, zu der das im <span class="varname"> angegebene </span> aufgelöst wird (siehe <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Objekt-ID-Übersetzung</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
