---
description: Adressenfilterelement. Optional in <Regel> - und <Pfadregel> -Elementen.
solution: Experience Manager
title: Adressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# Adressfilter{#addressfilter}

Adressenfilterelement. Optional in `<rule>` - und `<pathrule>` -Elementen.

Überschreibt `attribute::ClientAddressFilter` bei Anwendung der Regel.

## Attribute {#section-31e9ad29e9934933ac154bccbc729172}

Keine.

## Daten {#section-c762bdfe425140d689ea5abf25e9a48a}

Kommagetrennte Liste von IP-Adressen. Jede einzelne Adresse kann ein optionales Suffix für die Netmask enthalten, um die Angabe von IP-Adressbereichen zu ermöglichen. Weitere Informationen finden Sie unter `attribute::ClientAddressFilter` .

## Beschreibung {#section-d561b2485e004ef8a2085997d0f4bca6}

Der Zugriff auf diesen Bildkatalog kann auf eine oder mehrere bestimmte Client-IP-Adressen beschränkt werden, indem sie in einem `<addressfilter>` -Element spezifiziert werden. Der Fehler &quot;Anfrage verweigert&quot;wird an den Client zurückgegeben, wenn die Client-IP-Adresse nicht übereinstimmt.

Der Zugriff ist nicht beschränkt, wenn `<addressfilter>` leer oder nicht angegeben ist.

Wenn das Element `<expression>` im Element `<rule>` fehlt oder leer ist, wird `<addressfilter>` auf alle Anforderungen angewendet.

## Verwandte Themen {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
