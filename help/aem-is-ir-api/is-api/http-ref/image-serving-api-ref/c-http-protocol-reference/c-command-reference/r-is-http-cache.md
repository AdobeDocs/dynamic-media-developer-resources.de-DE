---
title: Cache
description: Cache-Steuerung Ermöglicht die selektive Deaktivierung der Client-seitigen Zwischenspeicherung (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und die Zwischenspeicherung im internen  [!DNL Platform Server] .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# Cache{#cache}

Cache-Steuerung Ermöglicht die selektive Deaktivierung des Client-seitigen Caching (Browser, Proxy-Server, Netzwerk-Caching-Systeme) und Caching im internen [!DNL Platform Server].

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ein|aus|validieren|aktualisieren</span> </p> </td> 
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

Wenn nur ein `*`cacheControl`*`-Wert angegeben ist, wird er sowohl auf den Client- als auch auf den Server-Cache angewendet.

Mit dem `validate`-Schlüsselwort können Cache-Einträge nach der Änderung von Bilddateien aktualisiert werden, ohne darauf warten zu müssen, dass der Cache-Eintrag automatisch abläuft. Die Client-Zwischenspeicherung ist von diesem Befehl nicht betroffen.

Das `update`-Schlüsselwort kann verwendet werden, um eine Aktualisierung der Server-seitigen Cache-Einträge zu erzwingen. Dies ist nützlich, nachdem Ressourcen geändert wurden, die nicht direkt vom Cache-Validierungsmechanismus verfolgt werden, z. B. wenn eine Schriftartdatei geändert wird, ohne den Dateinamen oder die zugehörige Schriftart-ID zu ändern.

Wenn in einer verschachtelten Anfrage angegeben, ermöglicht `cache=on` ein persistentes, Server-seitiges Caching des durch die verschachtelte Anfrage generierten Bildes. Es sollte darauf geachtet werden, dass das Caching für verschachtelte Anfragen nur dann aktiviert wird, wenn erwartet wird, dass dieselbe verschachtelte Anfrage wiederholt mit genau denselben Parametern aufgerufen wird.

## Eigenschaften {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Anforderungsattribut. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet. Wird ignoriert, wenn die Anfrage kein Antwortbild zurückgibt. *`clientControl`* wird ignoriert, wenn die Client-seitige Zwischenspeicherung vom Bildkatalog deaktiviert wird (wenn `catalog::Expiration` einen negativen Wert aufweist).

Die Client-seitige Cache-Steuerung (nur `on` und `off`) ist auch für statische Inhaltsanfragen unter [!DNL /is/content/] verfügbar.

## Standard {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` für HTTP-Anfragen, `cache=off` für verschachtelte/eingebettete Anfragen, `cache=on` für statische Inhaltsanfragen.

## Verwandte Themen {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
