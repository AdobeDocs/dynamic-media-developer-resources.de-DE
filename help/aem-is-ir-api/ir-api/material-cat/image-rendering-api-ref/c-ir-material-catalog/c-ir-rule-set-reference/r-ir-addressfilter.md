---
description: Adressfilterelement. Optional in <rule>-Elementen. Überschreibt das Attribut ClientAddressFilter, wenn die Regel angewendet wird.
solution: Experience Manager
title: adressfilter
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---


# adressfilter{#addressfilter}

Adressfilterelement. Optional in `<rule>`-Elementen. Überschreibt das Attribut::ClientAddressFilter, wenn die Regel angewendet wird.

## Attribute {#section-e7a0960f7f0045da91de37824aa4aeaa}

Keine.

## Daten {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Kommagetrennte Liste von IP-Adressen. Jede einzelne Adresse kann ein optionales Suffix &quot;netmask&quot;enthalten, um die Angabe der IP-Adressbereiche zu ermöglichen. Weitere Informationen finden Sie unter ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`.

## Beschreibung {#section-099b7839c4be40c68cbff29dad14e7d5}

Der Zugriff auf diesen Bildkatalog kann auf eine oder mehrere bestimmte IP-Adressen beschränkt werden, indem sie in einem `<addressfilter>`-Element angegeben werden. Der Fehler &quot;Anforderung verweigert&quot;wird an den Client zurückgegeben, wenn die Client-IP-Adresse nicht übereinstimmt.

Der Zugriff ist nicht eingeschränkt, wenn `<addressfilter>` leer oder nicht angegeben ist.

Wenn das Element `<expression>` im Element `<rule>` fehlt oder leer ist, wird das Element `<addressfilter>` auf alle Anforderungen angewendet.

`localhost` ist immer implizit Teil der  `ClientAddressFilter` Definition, auch wenn nicht explizit angegeben. Anforderungen, die von `localhost` stammen, werden unabhängig von der `ClientAddressFilter`-Spezifikation nie abgelehnt.

## SeeaAuch {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
