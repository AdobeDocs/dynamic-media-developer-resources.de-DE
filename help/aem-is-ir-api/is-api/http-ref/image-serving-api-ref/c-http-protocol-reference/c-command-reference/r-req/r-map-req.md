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
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Gibt `catalog::Map` ohne Änderungen zurück, wenn ein einfacher Katalogeintrag ohne zusätzliche angegebene Befehle abgefragt wird (wird nicht auf `catalog::maxPix` skaliert).

Wenn in der Anfrage andere Befehle angegeben sind, wird eine zusammengesetzte Imagemap zurückgegeben. Die zusammengesetzte Imagemap wird durch Skalieren, Zuschneiden, Drehen und Überlagern aller in der Anfrage enthaltenen `catalog::Map`- und/oder `map=`-Befehle abgeleitet, genau wie die Bilddaten mit `req=img` wären.

Geben Sie `text` zweiten Parameter an, oder lassen Sie ihn weg, damit Sie die Imagemap-Daten in Form einer Zeichenfolge des `HTML <AREA>` Elements mit dem Antwort-MIME-Typ `text/plain` zurückgeben können.

Geben Sie `xml` an, damit Sie die Antwort als XML anstatt als HTML formatieren können. Die Textkodierung kann optional angegeben werden. Der Standardwert lautet `UTF-8`.

Gibt eine leere Zeichenfolge (oder ein leeres `<AREA>`) zurück, wenn für die angegebenen Katalogobjekte keine Zuordnungsdaten gefunden wurden und/oder wenn nach dem Zuschneiden der Bilder keine `<AREA>` verbleiben.

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

Der `<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert lautet `s7jsonResponse`.

Siehe [Imagemaps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
