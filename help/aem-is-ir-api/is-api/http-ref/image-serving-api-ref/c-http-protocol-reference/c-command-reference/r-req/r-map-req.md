---
description: Imagemap-Daten.
seo-description: Imagemap-Daten.
seo-title: Karte
solution: Experience Manager
title: Karte
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Karte{#map}

Imagemap-Daten.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Gibt `catalog::Map` bei der Abfrage eines einfachen Katalogeintrags ohne zusätzliche Befehle ohne Änderung zurück (wird nicht skaliert auf `catalog::maxPix`).

Wenn andere Befehle in der Anforderung angegeben sind, wird eine Composite-Imagemap zurückgegeben, die durch Skalieren, Beschneiden, Drehen und Überlagern aller `catalog::Map` und/oder `map=` Befehle in der Anforderung abgeleitet wird, genau wie die Bilddaten mit `req=img`.

Geben Sie den zweiten Parameter an `text` oder lassen Sie ihn weg, um die Imagemap-Daten in Form einer `HTML <AREA>` Element-Zeichenfolge mit AntwortmIME-Typ zurückzugeben `text/plain`.

Geben Sie `xml` an, die Antwort als XML anstatt als HTML zu formatieren. Die Textkodierung kann optional angegeben werden. The default is `UTF-8`.

Gibt eine leere Zeichenfolge (oder ein leeres `<AREA>` Element) zurück, wenn für die angegebenen Katalogobjekte keine Zuordnungsdaten gefunden wurden und/oder wenn nach dem Beschneiden der Bilder keine `<AREA>` Elemente mehr vorhanden sind.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.

See [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
