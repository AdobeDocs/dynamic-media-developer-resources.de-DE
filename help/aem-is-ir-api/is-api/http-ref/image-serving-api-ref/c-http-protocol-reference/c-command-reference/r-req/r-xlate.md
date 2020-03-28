---
description: Verfügbare Gebietsschema-spezifische Versionen. Gibt eine Liste der verfügbaren Gebietsschema-spezifischen Versionen der Katalog-ID zurück, die im Anforderungspfad angegeben ist.
seo-description: Verfügbare Gebietsschema-spezifische Versionen. Gibt eine Liste der verfügbaren Gebietsschema-spezifischen Versionen der Katalog-ID zurück, die im Anforderungspfad angegeben ist.
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Siehe Übersetzung [der Objekt-ID](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Beispiel:

`xlate.translatedIds=image,image_fr,image_de`

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
