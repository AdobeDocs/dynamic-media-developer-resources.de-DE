---
title: cache
description: Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und der Zwischenspeicherung im internen [!DNL Platform Server] zwischenspeichern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---

# cache {#cache}

Cache-Steuerung. Hiermit können Sie die clientseitige Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und Zwischenspeicherung im internen [!DNL Platform Server] zwischenspeichern.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | off | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on | off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on | off </p></td> 
 </tr> 
</table>

Wenn nur eine *`cacheControl`* -Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Der `validate`&#39; Keyword ermöglicht die Aktualisierung von Server-Cache-Einträgen, nachdem Textur- oder Vignettendateien geändert wurden, ohne dass der Cache-Eintrag automatisch ablaufen muss. Die Client-Zwischenspeicherung ist von diesem Befehl nicht betroffen.

Wenn in einer verschachtelten Anforderung angegeben, `cache=on` ermöglicht das persistente, serverseitige Caching des Bildes, das von der verschachtelten Anforderung generiert wurde. Stellen Sie sicher, dass Sie die Zwischenspeicherung für verschachtelte Anforderungen nur aktivieren, wenn dieselbe verschachtelte Anforderung wiederholt mit denselben Parametern aufgerufen wird.

## Eigenschaften {#section-0dcbd62e1122400e8c347f408f2d937e}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. Die Eigenschaft *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Materialkatalog deaktiviert wird (wenn `attribute::Expiration` einen negativen Wert hat). Die Eigenschaft *`serverControl`* wird ignoriert, wenn die Zwischenspeicherung des Servers deaktiviert ist ( `PlatformServer::cache.enable`).

## Standard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Bei HTTP-Anforderungen: `cache=off` für verschachtelte/eingebettete Anforderungen.

## Verwandte Themen {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
