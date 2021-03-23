---
description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-title: cache
solution: Experience Manager
title: cache
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# cache{#cache}

Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
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

Wenn nur ein *`cacheControl`*-Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Anforderungsattribut. Wird ignoriert, wenn die Anforderung kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung durch den Bildkatalog deaktiviert ist (wenn ein negativer Wert  `catalog::Expiration` vorliegt).

Die Standardeinstellung ist `cache=on,on`.
