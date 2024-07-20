---
description: Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und des Caching im internen [!DNL Platform Server] Cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# cache{#cache}

Cache-Steuerung. Ermöglicht das selektive Deaktivieren der clientseitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerkzwischenspeicherungssysteme) und des Caching im internen [!DNL Platform Server]-Cache.

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

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

Wenn nur ein *`cacheControl`* -Wert angegeben ist, wird er sowohl auf Client- als auch auf Server-Caches angewendet.

Anforderungsattribut. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die clientseitige Zwischenspeicherung vom Bildkatalog deaktiviert wird (wenn `catalog::Expiration` einen negativen Wert aufweist).

Der Standardwert ist `cache=on,on`.
