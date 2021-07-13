---
description: Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und der Zwischenspeicherung im internen Platform Server-Cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# cache{#cache}

Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und der Zwischenspeicherung im internen Platform Server-Cache.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on_off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on_off</span> </p></td> 
 </tr> 
</table>

Wenn nur ein `*`cacheControl`*` -Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Das `validate`-Keyword ermöglicht die Aktualisierung von Cache-Einträgen nach einer Änderung der Bilddateien, ohne darauf warten zu müssen, dass der Cache-Eintrag automatisch abläuft. Die Client-Zwischenspeicherung ist von diesem Befehl nicht betroffen.

Mit dem Keyword `update` können Sie erzwingen, serverseitige Cache-Einträge zu aktualisieren. Dies ist nützlich, nachdem Ressourcen geändert wurden, die nicht direkt vom Cache-Überprüfungsmechanismus verfolgt werden, z. B. wenn eine Schriftartdatei geändert wird, ohne den Dateinamen oder die zugehörige Schriftart-ID zu ändern.

Wenn in einer verschachtelten Anforderung angegeben, ermöglicht `cache=on` das beständige, serverseitige Caching des von der verschachtelten Anforderung generierten Bildes. Es sollte darauf geachtet werden, die Zwischenspeicherung für verschachtelte Anforderungen nur zu aktivieren, wenn erwartet wird, dass dieselbe verschachtelte Anforderung wiederholt mit genau denselben Parametern aufgerufen wird.

## Eigenschaften {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. *`clientControl`*wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Bildkatalog deaktiviert wird (wenn `catalog::Expiration` einen negativen Wert hat).

Die clientseitige Cache-Steuerung ( `on` und `off`) ist auch für statische Inhaltsanforderungen unter [!DNL /is/content/] verfügbar.

## Standard {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` für HTTP-Anforderungen  `cache=off` für verschachtelte/eingebettete Anforderungen  `cache=on` für statische Inhaltsanforderungen.

## Verwandte Themen {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
