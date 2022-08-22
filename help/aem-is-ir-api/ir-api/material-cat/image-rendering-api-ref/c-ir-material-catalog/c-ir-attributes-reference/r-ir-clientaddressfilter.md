---
title: ClientAddressFilter
description: Filter für Client-IP-Adressen. Ermöglicht die Spezifikation einer oder mehrerer IP-Adressen oder Adressbereiche.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Filter für Client-IP-Adressen. Ermöglicht die Spezifikation einer oder mehrerer IP-Adressen oder Adressbereiche.

Wenn diese Option spezifiziert ist, werden Anfragen an diesen Bildkatalog, die von einem Client stammen, der eine nicht aufgeführte IP-Adresse hat, abgelehnt. `localhost` ist immer implizit Teil der `ClientAddressFilter` -Definition, auch wenn nicht explizit angegeben. Von `localhost` werden nie abgelehnt, unabhängig von der `ClientAddressFilter` Spezifikation.

## Eigenschaften {#section-21a2992f108d42fb8660c0d65aa61e13}

Kommagetrennte Liste von IP-Adressen mit optionalen Masken ([CIDR-Notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) verwendet wird):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP-Adresse in *[!DNL ddd.ddd.ddd.ddd]* format

* *[!DNL netmask]* Netzmaske (0...32)

Dieses Attribut wird ignoriert, wenn eine Vorverarbeitungsregel mit einer `<addressfilter>` -Element angewendet wird.

## Standard {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Vererbt von `default::AddressFilter` wenn nicht definiert oder leer ist.

## Beispiele {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Keine Zugriffsbeschränkungen: `0.0.0.0/0`
* Zugriff auf alle Adressen gewähren, die mit beginnen `192: 192.0.0.0/8`
* Zugriff auf 512 Hosts mit Adressen zwischen `192.168.12.0` und `192.168.13.255: 192.168.12.0/23`

* Zugriff auf eine einzelne IP-Adresse gewähren: `192.168.2.117` oder `192.168.2.117/32`

## Verwandte Themen {#section-6198780c7b3045aabd211eefb38bc565}

[Adressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
