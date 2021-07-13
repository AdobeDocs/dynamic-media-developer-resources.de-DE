---
description: Verfügbare gebietsschemaspezifische Versionen. Gibt eine Liste der verfügbaren gebietsschemaspezifischen Versionen der im Anfragepfad angegebenen Katalog-ID zurück.
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# xlate{#xlate}

Verfügbare gebietsschemaspezifische Versionen. Gibt eine Liste der verfügbaren gebietsschemaspezifischen Versionen der im Anfragepfad angegebenen Katalog-ID zurück.

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

Anforderungen, die das JSONP-Antwortformat unterstützen, ermöglichen es Ihnen, den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` anzugeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
