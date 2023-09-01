---
title: Karte
description: Imagemap-Daten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# Karte{#map}

Imagemap-Daten.

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

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

Rückgabe `catalog::Map` ohne Änderung bei der Abfrage eines einfachen Katalogeintrags ohne zusätzliche Befehle angegeben (skaliert nicht auf `catalog::maxPix`).

Wenn andere Befehle in der Anfrage angegeben sind, wird eine zusammengesetzte Imagemap zurückgegeben. Die Composite-Imagemap wird durch Skalieren, Zuschneiden, Drehen und Überlagern aller `catalog::Map` und/oder `map=` -Befehle, die in der Anfrage enthalten sind, genau wie die Bilddaten mit `req=img`.

Angeben `text` oder lassen Sie den zweiten Parameter weg, damit Sie die Imagemap-Daten in Form einer `HTML <AREA>` Elementzeichenfolge mit Antwort-MIME-Typ `text/plain`.

Angeben `xml` sodass Sie die Antwort als XML anstatt als HTML formatieren können. Die Textkodierung kann optional angegeben werden. Der Standardwert ist `UTF-8`.

Gibt eine leere Zeichenfolge aus (oder leer) `<AREA>` -Element) wenn keine Zuordnungsdaten für die angegebenen Katalogobjekte gefunden wurden und/oder wenn keine `<AREA>` -Elemente bleiben nach dem Zuschneiden der Bilder erhalten.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration`.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax von `req=` Parameter:

`req=...,json [&handler = reqHandler ]`

Die `<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Siehe [Imagemaps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
