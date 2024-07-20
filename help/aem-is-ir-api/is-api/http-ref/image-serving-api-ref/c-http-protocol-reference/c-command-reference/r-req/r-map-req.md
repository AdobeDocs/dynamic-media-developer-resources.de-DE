---
title: Karte
description: Imagemap-Daten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Karte{#map}

Imagemap-Daten.

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Gibt `catalog::Map` ohne Änderung zurück, wenn ein einfacher Katalogeintrag ohne zusätzliche Befehle abgefragt wird (nicht skaliert auf `catalog::maxPix`).

Wenn andere Befehle in der Anfrage angegeben sind, wird eine zusammengesetzte Imagemap zurückgegeben. Die Composite-Imagemap wird durch Skalieren, Zuschneiden, Drehen und Überlagern aller in der Anfrage enthaltenen Befehle `catalog::Map` und/oder `map=` abgeleitet, genau wie die Bilddaten mit `req=img`.

Geben Sie `text` an oder lassen Sie den zweiten Parameter weg, damit Sie die Imagemap-Daten in Form einer `HTML <AREA>` -Elementzeichenfolge mit Antwort-MIME-Typ `text/plain` zurückgeben können.

Geben Sie `xml` an, damit Sie die Antwort als XML anstatt als HTML formatieren können. Die Textkodierung kann optional angegeben werden. Der Standardwert ist `UTF-8`.

Gibt eine leere Zeichenfolge (oder ein leeres `<AREA>` -Element) zurück, wenn für die angegebenen Katalogobjekte keine Zuordnungsdaten gefunden wurden und/oder wenn nach dem Zuschneiden der Bilder keine `<AREA>` -Elemente verbleiben.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

Der `<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Siehe [Imagemaps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
