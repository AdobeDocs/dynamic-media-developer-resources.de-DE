---
description: Verfügbare gebietsschemaspezifische Versionen Gibt eine Liste der verfügbaren gebietsschemaspezifischen Versionen der im Anfragepfad angegebenen Katalog-ID zurück.
solution: Experience Manager
title: spätplattieren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---

# spätplattieren{#xlate}

Verfügbare gebietsschemaspezifische Versionen Gibt eine Liste der verfügbaren gebietsschemaspezifischen Versionen der im Anfragepfad angegebenen Katalog-ID zurück.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Siehe [Objekt-ID-](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Beispiel:

`xlate.translatedIds=image,image_fr,image_de`

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
