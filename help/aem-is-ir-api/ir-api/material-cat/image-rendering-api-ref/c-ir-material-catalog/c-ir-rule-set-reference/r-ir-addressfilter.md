---
description: Filterelement der Adresse. Optional in <rule>-Elementen. Überschreibt das ClientAddressFilter-Attribut, wenn die Regel angewendet wird.
solution: Experience Manager
title: addressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---

# addressFilter{#addressfilter}

Filterelement der Adresse. Optional in `<rule>`. Überschreibt das Attribut::ClientAddressFilter, wenn die Regel angewendet wird.

## Attribute {#section-e7a0960f7f0045da91de37824aa4aeaa}

Keine.

## Daten {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Liste der IP-Adressen (durch Kommata getrennt) Jede einzelne Adresse kann ein optionales Netzmasken-Suffix enthalten, um die Angabe von IP-Adressbereichen zu ermöglichen. Siehe [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) für Details.

## Beschreibung {#section-099b7839c4be40c68cbff29dad14e7d5}

Der Zugriff auf diesen Bildkatalog kann auf eine oder mehrere bestimmte IP-Adressen beschränkt werden, indem diese in einem `<addressfilter>` angegeben werden. Der Fehler „Anfrage abgelehnt“ wird an den Client zurückgegeben, wenn die Client-IP-Adresse nicht übereinstimmt.

Der Zugriff ist nicht eingeschränkt, wenn `<addressfilter>` leer oder nicht angegeben ist.

Wenn die `<expression>` im `<rule>` fehlt oder leer ist, wird die `<addressfilter>` auf alle Anfragen angewendet.

`localhost` ist immer implizit Teil der `ClientAddressFilter`, auch wenn sie nicht explizit angegeben ist. Anfragen, die von `localhost` stammen, werden unabhängig von der `ClientAddressFilter` nie zurückgewiesen.

## Siehe auch {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
