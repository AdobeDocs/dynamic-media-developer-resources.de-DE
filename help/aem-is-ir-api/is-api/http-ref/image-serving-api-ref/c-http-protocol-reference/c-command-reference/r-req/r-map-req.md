---
description: Imagemap-Daten.
solution: Experience Manager
title: Karte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---

# Karte{#map}

Imagemap-Daten.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Gibt `catalog::Map` ohne Änderung zurück, wenn ein einfacher Katalogeintrag ohne zusätzliche Befehle abgefragt wird (wird nicht auf `catalog::maxPix` skaliert).

Wenn andere Befehle in der Anfrage angegeben sind, wird eine zusammengesetzte Imagemap zurückgegeben, die durch Skalieren, Zuschneiden, Drehen und Überlagern aller in der Anfrage enthaltenen `catalog::Map`- und/oder `map=`-Befehle abgeleitet wird, genau wie die Bilddaten mit `req=img`.

Geben Sie `text` an oder lassen Sie den zweiten Parameter weg, um die Imagemap-Daten in Form einer `HTML <AREA>`-Elementzeichenfolge mit Antwort-MIME-Typ `text/plain` zurückzugeben.

Geben Sie `xml` an, um die Antwort als XML anstelle von HTML zu formatieren. Die Textkodierung kann optional angegeben werden. Der Standardwert ist `UTF-8`.

Gibt eine leere Zeichenfolge (oder ein leeres `<AREA>`-Element) zurück, wenn für die angegebenen Katalogobjekte keine Zuordnungsdaten gefunden wurden und/oder wenn nach dem Zuschneiden der Bilder keine `<AREA>`-Elemente mehr vorhanden sind.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

Anforderungen, die das JSONP-Antwortformat unterstützen, ermöglichen es Ihnen, den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` anzugeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.

Siehe [Imagemaps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
