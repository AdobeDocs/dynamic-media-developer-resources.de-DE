---
description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-title: cache
solution: Experience Manager
title: cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on| off| validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on| off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on| off </p></td> 
 </tr> 
</table>

Wenn nur ein *`cacheControl`* Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Das Schlüsselwort &#39; `validate`&#39; ermöglicht die Aktualisierung von Server-Cache-Einträgen nach einer Änderung der Textur- oder Vignettendateien, ohne dass der Cache-Eintrag automatisch ablaufen muss. Die Zwischenspeicherung im Client wird von diesem Befehl nicht beeinflusst.

Wenn dies in einer verschachtelten Anforderung angegeben ist, `cache=on` wird die permanente, serverseitige Zwischenspeicherung des von der verschachtelten Anforderung generierten Bildes aktiviert. Es sollte darauf geachtet werden, dass die Zwischenspeicherung für verschachtelte Anforderungen nur aktiviert wird, wenn erwartet wird, dass dieselbe verschachtelte Anforderung wiederholt mit genau denselben Parametern aufgerufen wird.

## Eigenschaften {#section-0dcbd62e1122400e8c347f408f2d937e}

Kann an beliebiger Stelle in der Anforderung auftreten. Wird ignoriert, wenn die Anforderung kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung durch den Materialkatalog deaktiviert ist (wenn `attribute::Expiration` ein negativer Wert vorliegt). *`serverControl`* wird ignoriert, wenn die Serverzwischenspeicherung deaktiviert ist ( `PlatformServer::cache.enable`).

## Standard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` für HTTP-Anforderungen, `cache=off` für verschachtelte/eingebettete Anforderungen.

## Verwandte Themen {#section-2f5853751dab49579e97418fa766bdf9}

[Katalog::Ablauf](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
