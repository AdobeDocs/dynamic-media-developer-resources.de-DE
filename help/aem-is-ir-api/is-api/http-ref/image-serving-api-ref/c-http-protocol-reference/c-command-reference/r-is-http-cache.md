---
description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-title: cache
solution: Experience Manager
title: cache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---


# cache{#cache}

Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Wenn nur ein `*`cacheControl`*`-Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Das Schlüsselwort `validate` erlaubt das Aktualisieren von Cache-Einträgen, nachdem Bilddateien geändert wurden, ohne dass der Cache-Eintrag automatisch ablaufen muss. Die Zwischenspeicherung im Client wird von diesem Befehl nicht beeinflusst.

Mit dem Schlüsselwort `update` können Sie erzwingen, serverseitige Cache-Einträge zu aktualisieren. Dies ist nützlich, wenn Ressourcen geändert wurden, die nicht direkt vom Cache-Überprüfungsmechanismus verfolgt werden, z. B. wenn eine Schriftartdatei ohne Änderung des Dateinamens oder der zugehörigen Schriftart-ID geändert wird.

Wenn in einer verschachtelten Anforderung angegeben, aktiviert `cache=on` die permanente, serverseitige Zwischenspeicherung des von der verschachtelten Anforderung generierten Bildes. Es sollte darauf geachtet werden, dass die Zwischenspeicherung für verschachtelte Anforderungen nur aktiviert wird, wenn erwartet wird, dass dieselbe verschachtelte Anforderung wiederholt mit genau denselben Parametern aufgerufen wird.

## Eigenschaften {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn die Anforderung kein Antwortbild zurückgibt. *`clientControl`*wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Bildkatalog deaktiviert wird (wenn `catalog::Expiration` einen negativen Wert hat).

Clientseitige Cache-Steuerung ( `on` und `off`) ist auch für statische Inhaltsanforderungen unter [!DNL /is/content/] verfügbar.

## Standard {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` für HTTP-Anforderungen,  `cache=off` für verschachtelte/eingebettete Anforderungen  `cache=on` für statische Inhaltsanforderungen.

## Verwandte Themen {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[Katalog::Ablauf](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
