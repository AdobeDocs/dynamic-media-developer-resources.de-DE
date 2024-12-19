---
description: Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.

Wenn diese Option angegeben ist, werden Anfragen an diesen Bildkatalog abgelehnt, wenn sie von einem Client stammen, der eine nicht aufgeführte IP-Adresse hat.

## Eigenschaften {#section-d785265988324af68835410c9ba54147}

Durch Kommas getrennte Liste von IP-Adressen mit optionalen Netzmasken (CIDR-Notation wird verwendet):

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> IP-Adresse</span> </p> </td> 
  <td class="stentry"> <p>IP-Adresse <span class="varname"> Format ddd.ddd.ddd.ddd</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Netzmaske</span> </p></td> 
  <td class="stentry"> <p>Netzmaske (0…32). </p></td> 
 </tr> 
</table>

Dieses Attribut wird ignoriert, wenn eine Vorverarbeitungsregel mit einem `<addressfilter>` angewendet wird.

## Standard {#section-de26e8c9225745e985e4beac1f03f4f6}

Von `default::AddressFilter` geerbt, wenn nicht definiert oder leer.

## Beispiele {#section-a955314d2b6a4213a16c12a8b18d8627}

Keine Zugriffsbeschränkungen: `0.0.0.0/0`

Zugriff auf alle Adressen ab 192 gewähren: `192.0.0.0/8`

Gewähren des Zugriffs auf die 512 Hosts mit Adressen zwischen 192.168.12.0 und 192.168.13.255: `192.168.12.0/23`

Zugriff auf eine einzelne IP-Adresse gewähren: `192.168.2.117` oder `192.168.2.117/32`

## Verwandte Themen {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
