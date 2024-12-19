---
description: Cache-Steuerung Ermöglicht die selektive Deaktivierung der Client-seitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und die Zwischenspeicherung im internen  [!DNL Platform Server] .
solution: Experience Manager
title: Cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Cache{#cache}

Cache-Steuerung Ermöglicht die selektive Deaktivierung des Client-seitigen Caching (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und Caching im internen [!DNL Platform Server].

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ein|aus</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ein|aus</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ein|aus</span> </p></td> 
 </tr> 
</table>

Wenn nur ein *`cacheControl`* angegeben ist, wird er sowohl auf den Client- als auch auf den Server-Cache angewendet.

Anforderungsattribut. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die Client-seitige Zwischenspeicherung vom Bildkatalog deaktiviert wird (wenn `catalog::Expiration` einen negativen Wert aufweist).

Die Standardeinstellung ist `cache=on,on`.
