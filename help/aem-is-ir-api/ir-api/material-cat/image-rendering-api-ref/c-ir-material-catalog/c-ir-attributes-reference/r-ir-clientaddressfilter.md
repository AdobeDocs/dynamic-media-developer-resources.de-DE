---
description: Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.
seo-description: Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.

Wenn dies angegeben ist, werden Anforderungen an diesen Bildkatalog, die von einem Client an einer nicht aufgelisteten IP-Adresse stammen, abgelehnt. `localhost` ist immer implizit Teil der `ClientAddressFilter` Definition, auch wenn nicht explizit angegeben. Anfragen, die von `localhost` uns stammen, werden unabhängig von der `ClientAddressFilter` Spezifikation nie abgelehnt.

## Eigenschaften {#section-21a2992f108d42fb8660c0d65aa61e13}

Kommagetrennte Liste von IP-Adressen mit optionalen Netmboxes ([CIDR-Notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) wird verwendet):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP-Adresse in *[!DNL ddd.ddd.ddd.ddd]* Format

* *[!DNL netmask]* Netzmaske (0...32)

Dieses Attribut wird ignoriert, wenn eine Vorverarbeitungsregel mit einem `<addressfilter>` Element angewendet wird.

## Standard {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Vererbt von, `default::AddressFilter` wenn nicht definiert oder leer.

## Beispiele {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Keine Zugriffsbeschränkungen: `0.0.0.0/0`
* Zugriff auf alle Adressen gewähren, beginnend mit `192: 192.0.0.0/8`
* Gewähren Sie Zugriff auf die 512 Hosts mit Adressen zwischen `192.168.12.0` und `192.168.13.255: 192.168.12.0/23`

* Zugriff auf eine einzelne IP-Adresse gewähren: `192.168.2.117` oder `192.168.2.117/32`

## Verwandte Themen {#section-6198780c7b3045aabd211eefb38bc565}

[adressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
