---
description: Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und der Zwischenspeicherung im internen Platform Server-Cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# cache{#cache}

Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und der Zwischenspeicherung im internen Platform Server-Cache.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | off | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>on | off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>on | off </p></td> 
 </tr> 
</table>

Wenn nur ein *`cacheControl`* -Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Das Keyword &quot; `validate`&quot;ermöglicht die Aktualisierung von Server-Cache-Einträgen nach Änderung der Textur- oder Vignettendateien, ohne dass der Cache-Eintrag automatisch ablaufen muss. Die Client-Zwischenspeicherung ist von diesem Befehl nicht betroffen.

Wenn in einer verschachtelten Anforderung angegeben, ermöglicht `cache=on` das beständige, serverseitige Caching des von der verschachtelten Anforderung generierten Bildes. Es sollte darauf geachtet werden, die Zwischenspeicherung für verschachtelte Anforderungen nur zu aktivieren, wenn erwartet wird, dass dieselbe verschachtelte Anforderung wiederholt mit genau denselben Parametern aufgerufen wird.

## Eigenschaften {#section-0dcbd62e1122400e8c347f408f2d937e}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Materialkatalog deaktiviert wird (wenn  `attribute::Expiration` einen negativen Wert aufweist). *`serverControl`* wird ignoriert, wenn die Zwischenspeicherung des Servers deaktiviert ist (  `PlatformServer::cache.enable`).

## Standard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` für HTTP-Anforderungen  `cache=off` für verschachtelte/eingebettete Anforderungen.

## Verwandte Themen {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
