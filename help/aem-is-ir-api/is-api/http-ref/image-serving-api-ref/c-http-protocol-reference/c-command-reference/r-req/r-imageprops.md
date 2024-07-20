---
description: Source-Bildeigenschaften. Gibt ausgewählte Eigenschaften der im URL-Pfad angegebenen Bilddatei oder des Katalogeintrags zurück.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 4%

---

# imageprops{#imageprops}

Source-Bildeigenschaften. Gibt ausgewählte Eigenschaften der im URL-Pfad angegebenen Bilddatei oder des Katalogeintrags zurück.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `attribute::NonImgExpiration` basiert.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

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
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> oder der standardmäßige Ankerpunkt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> doppelt </p> </td> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> oder die Standardzeit für die Live-Schaltung </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Bildhöhe mit voller Auflösung in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Name/Beschreibung des mit diesem Bild verknüpften Profils </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Bild. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das verknüpfte Profil in das Bild eingebettet ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded FotoshopPaths</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das Bild Photoshop-Pfaddaten enthält </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Bild. embeddedXmpData</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das Bild XMP Daten enthält </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 für keine Maske, 1 für vormultipliziertes Alpha, 2 für nicht-vormultipliziertes Alpha und 3 für ein separates Maskenbild </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> oder leer, wenn kein Katalogeintrag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Bild. photoshopPathNames</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Kommagetrennte Liste der Namen aller mit diesem Bild verknüpften Photoshop-Pfade </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Bildtyp: "CMYK", "RGB"oder "BW"(bei Graustufenbildern) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModifier</span> oder leer, wenn kein Katalogeintrag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> Standarddruckauflösung in Pixel/Zoll </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> oder die standardmäßige Objektauflösung </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p>Änderungsdatum/-uhrzeit (aus <span class="codeph"> Katalog::TimeStamp</span> oder der Bilddatei) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbRes</span> oder die standardmäßige Miniaturauflösung </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbType</span> oder der standardmäßige Miniaturtyp </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Bildbreite mit voller Auflösung in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Katalog-ID, auf die das im Pfad angegebene <span class="varname"> Objekt</span> aufgelöst wird (siehe <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Übersetzung der Objekt-ID</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
