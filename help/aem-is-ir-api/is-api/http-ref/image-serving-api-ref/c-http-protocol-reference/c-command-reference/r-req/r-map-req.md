---
title: Karte
description: Imagemap-Daten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
TQID: 'https://experienceleague.adobe.com/Ly1JWjeEyZWUEiyVcv-t-OKf0cp6uuMsbR0B6BE1fhY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
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
