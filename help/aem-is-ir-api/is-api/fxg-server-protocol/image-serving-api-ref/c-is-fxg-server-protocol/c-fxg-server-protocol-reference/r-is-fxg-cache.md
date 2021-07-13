---
description: Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und der Zwischenspeicherung im internen Platform Server-Cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# cache{#cache}

Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und der Zwischenspeicherung im internen Platform Server-Cache.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on_off</span> </p></td> 
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

Wenn nur ein *`cacheControl`* -Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Anforderungsattribut. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Bildkatalog deaktiviert wird (wenn  `catalog::Expiration` einen negativen Wert aufweist).

Die Standardeinstellung ist `cache=on,on`.
