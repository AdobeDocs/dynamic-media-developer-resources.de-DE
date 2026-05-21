---
title: ClientAddressFilter
description: Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
TQID: 'https://experienceleague.adobe.com/azMITpRcITTOEB0FCev6vWiTmocumP-0HTQD3rIV-fA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 2%

---

# ClientAddressFilter{#clientaddressfilter}

Client-IP-Adressfilter. Ermöglicht die Angabe einer oder mehrerer IP-Adressen oder Adressbereiche.

Wenn diese Option angegeben ist, werden Anfragen an diesen Bildkatalog abgelehnt, wenn sie von einem Client stammen, der eine nicht aufgeführte IP-Adresse hat. `localhost` ist immer implizit Teil der `ClientAddressFilter`, auch wenn sie nicht explizit angegeben ist. Anfragen, die von `localhost` stammen, werden unabhängig von der `ClientAddressFilter` nie zurückgewiesen.

## Eigenschaften {#section-21a2992f108d42fb8660c0d65aa61e13}

Durch Kommas getrennte Liste von IP-Adressen mit optionalen Netzmasken ([CIDR-Notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) wird verwendet):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* IP-Adresse im *[!DNL ddd.ddd.ddd.ddd]* Format *[!DNL ipAddress]*

* *[!DNL netmask]* Netzmaske (0…32)

Dieses Attribut wird ignoriert, wenn eine Vorverarbeitungsregel mit einem `<addressfilter>` angewendet wird.

## Standard {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Von `default::AddressFilter` geerbt, wenn nicht definiert oder leer.

## Beispiele {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Keine Zugriffsbeschränkungen: `0.0.0.0/0`
* Zugriff auf alle Adressen ab `192: 192.0.0.0/8` gewähren
* Zugriff auf die 512 Hosts mit Adressen zwischen `192.168.12.0` und `192.168.13.255: 192.168.12.0/23` gewähren

* Zugriff auf eine einzelne IP-Adresse gewähren: `192.168.2.117` oder `192.168.2.117/32`

## Verwandte Themen {#section-6198780c7b3045aabd211eefb38bc565}

[addressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
