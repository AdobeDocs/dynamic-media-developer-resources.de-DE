---
title: Cache
description: Cache-Steuerung Ermöglicht die selektive Deaktivierung der Client-seitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und die Zwischenspeicherung im internen  [!DNL Platform Server] .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
TQID: 'https://experienceleague.adobe.com/xq-8hE9RB7I-CMb-yguhBcEttxTv6IRRHWzh0lDvn6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 1%

---

# Cache {#cache}

Cache-Steuerung Ermöglicht die selektive Deaktivierung des Client-seitigen Caching (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und des Caching im internen [!DNL Platform Server].

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | off | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl-</span> </p> </td> 
  <td class="stentry"> <p>Ein | Aus </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl-</span> </p></td> 
  <td class="stentry"> <p>Ein | Aus </p></td> 
 </tr> 
</table>

Wenn nur ein *`cacheControl`* angegeben ist, wird er sowohl auf den Client- als auch auf den Server-Cache angewendet.

Mit dem Schlüsselwort &quot;`validate`&quot; können Server-Cache-Einträge aktualisiert werden, nachdem sich die Textur- oder Vignettendateien geändert haben, ohne darauf warten zu müssen, dass der Cache-Eintrag automatisch abläuft. Die Client-Zwischenspeicherung ist von diesem Befehl nicht betroffen.

Wenn in einer verschachtelten Anfrage angegeben, ermöglicht `cache=on` ein persistentes, Server-seitiges Caching des durch die verschachtelte Anfrage generierten Bildes. Achten Sie darauf, dass Sie das Caching nur für verschachtelte Anfragen aktivieren, wenn dieselbe verschachtelte Anfrage wiederholt mit denselben Parametern aufgerufen wird.

## Eigenschaften {#section-0dcbd62e1122400e8c347f408f2d937e}

Kann überall in der Anfrage auftreten. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. Die Eigenschaft *`clientControl`* wird ignoriert, wenn die Client-seitige Zwischenspeicherung vom Materialkatalog deaktiviert wird (wenn `attribute::Expiration` einen negativen Wert hat). Die Eigenschaft *`serverControl`* wird ignoriert, wenn die Server-Zwischenspeicherung deaktiviert ist ( `PlatformServer::cache.enable`).

## Standard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Bei HTTP-Anfragen `cache=off` Sie für verschachtelte oder eingebettete Anfragen.

## Verwandte Themen {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
