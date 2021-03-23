---
description: Verfügbare Gebietsschema-spezifische Versionen. Gibt eine Liste der verfügbaren Gebietsschema-spezifischen Versionen der Katalog-ID zurück, die im Anforderungspfad angegeben ist.
seo-description: Verfügbare Gebietsschema-spezifische Versionen. Gibt eine Liste der verfügbaren Gebietsschema-spezifischen Versionen der Katalog-ID zurück, die im Anforderungspfad angegeben ist.
seo-title: xlate
solution: Experience Manager
title: xlate
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# xlate{#xlate}

Verfügbare Gebietsschema-spezifische Versionen. Gibt eine Liste der verfügbaren Gebietsschema-spezifischen Versionen der Katalog-ID zurück, die im Anforderungspfad angegeben ist.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Siehe [Objekt-ID-Übersetzung](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Beispiel:

`xlate.translatedIds=image,image_fr,image_de`

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
