---
description: Eigenschaften des Quellbilds. Gibt ausgewählte Eigenschaften der Bilddatei oder des Katalogeintrags zurück, die im URL-Pfad angegeben sind.
seo-description: Eigenschaften des Quellbilds. Gibt ausgewählte Eigenschaften der Bilddatei oder des Katalogeintrags zurück, die im URL-Pfad angegeben sind.
seo-title: imageprops
solution: Experience Manager
title: imageprops
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageprops{#imageprops}

Eigenschaften des Quellbilds. Gibt ausgewählte Eigenschaften der Bilddatei oder des Katalogeintrags zurück, die im URL-Pfad angegeben sind.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

The HTTP response is cacheable with the TTL based on `attribute::NonImgExpiration`.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.

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
   <td> <p> <span class="codeph"> Katalog::Anker</span> oder Standardankerpunkt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> doppelt </p> </td> 
   <td> <p> <span class="codeph"> Katalog::Ablauf</span> oder die standardmäßige Live-Zeit </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Bildhöhe in voller Auflösung in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Name/Beschreibung des Profils, das mit diesem Bild verknüpft ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Bild. eingebettetesIccProfile</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das zugehörige Profil in das Bild eingebettet ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.eingebettete FotoshopPaths</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das Bild Fotoshop-Pfaddaten enthält </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Bild. embeddedXmpData</span> </p> </td> 
   <td> <p> boolesch </p> </td> 
   <td> <p> 1, wenn das Bild XMP-Daten enthält </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 für keine Maske, 1 für vormultiplizierte Alpha, 2 für nicht vormultiplizierte Alpha und 3 für ein separates Maskenbild </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> <span class="codeph"> Katalog:Modifikator</span> oder leer, wenn kein Katalogeintrag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Bild. photoshopPathNames</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Kommagetrennte Liste der Namen aller Fotoshop-Pfade, die mit diesem Bild verknüpft sind </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Bildtyp kann "CMYK", "RGB"oder "BW"sein (bei Graustufenbildern) </p> </td> 
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
   <td> <p> <span class="codeph"> Katalog::Auflösung</span> oder Standardobjektauflösung </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p>Datum/Uhrzeit der Änderung (aus <span class="codeph"> Katalog::TimeStamp</span> oder der Bilddatei) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> Katalog::ThumbRes</span> oder die Standardauflösung für Miniaturansichten </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> Katalog::ThumbType</span> oder der standardmäßige Miniaturansichtentyp </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Bildbreite in voller Auflösung in Pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Katalog-ID, auf die das im Pfad angegebene <span class="varname"> Objekt</span> aufgelöst wird (siehe Übersetzung <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> der</a>Objekt-ID). </p> </td> 
  </tr> 
 </tbody> 
</table>

