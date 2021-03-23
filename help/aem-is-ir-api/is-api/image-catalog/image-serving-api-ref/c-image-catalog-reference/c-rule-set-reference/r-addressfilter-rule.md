---
description: Adressfilterelement. Optional in den Elementen <rule> und <pathrule>.
seo-description: Adressfilterelement. Optional in den Elementen <rule> und <pathrule>.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---


# adressfilter{#addressfilter}

Adressfilterelement. Optional in den Elementen `<rule>` und `<pathrule>`.

Überschreibt `attribute::ClientAddressFilter`, wenn die Regel angewendet wird.

## Attribute {#section-31e9ad29e9934933ac154bccbc729172}

Keine.

## Daten {#section-c762bdfe425140d689ea5abf25e9a48a}

Kommagetrennte Liste von IP-Adressen. Jede einzelne Adresse kann ein optionales Suffix &quot;netmask&quot;enthalten, um die Angabe der IP-Adressbereiche zu ermöglichen. Weitere Informationen finden Sie unter `attribute::ClientAddressFilter`.

## Beschreibung {#section-d561b2485e004ef8a2085997d0f4bca6}

Der Zugriff auf diesen Bildkatalog kann auf eine oder mehrere bestimmte Client-IP-Adressen beschränkt werden, indem sie in einem `<addressfilter>`-Element angegeben werden. Der Fehler &quot;Anforderung verweigert&quot;wird an den Client zurückgegeben, wenn die Client-IP-Adresse nicht übereinstimmt.

Der Zugriff ist nicht eingeschränkt, wenn `<addressfilter>` leer oder nicht angegeben ist.

Wenn das Element `<expression>` im Element `<rule>` fehlt oder leer ist, wird das Element `<addressfilter>` auf alle Anforderungen angewendet.

## Verwandte Themen {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
