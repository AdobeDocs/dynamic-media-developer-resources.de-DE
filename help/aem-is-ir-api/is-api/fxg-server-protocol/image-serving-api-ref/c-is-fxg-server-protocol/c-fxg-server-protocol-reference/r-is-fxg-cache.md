---
description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-description: Cachesteuerung. Ermöglicht die selektive Deaktivierung der clientseitigen Zwischenspeicherung (Browser, Proxyserver, Netzwerkzwischenspeichersysteme) und die Zwischenspeicherung im internen Platform Server-Cache.
seo-title: cache
solution: Experience Manager
title: cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Wenn nur ein *`cacheControl`* Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Anforderungsattribut. Wird ignoriert, wenn die Anforderung kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Bildkatalog deaktiviert ist (wenn `catalog::Expiration` ein negativer Wert vorliegt).

Defaults to `cache=on,on`.
