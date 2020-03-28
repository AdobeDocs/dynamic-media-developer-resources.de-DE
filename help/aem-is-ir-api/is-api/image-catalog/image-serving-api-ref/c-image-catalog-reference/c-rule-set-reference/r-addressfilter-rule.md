---
description: Adressfilterelement. Optional in den Elementen <rule> und <pathrule>.
seo-description: Adressfilterelement. Optional in den Elementen <rule> und <pathrule>.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# adressfilter{#addressfilter}

Adressfilterelement. Optional in `<rule>` und `<pathrule>` -Elementen.

Überschreibt, `attribute::ClientAddressFilter` wenn die Regel angewendet wird.

## Attribute {#section-31e9ad29e9934933ac154bccbc729172}

Keine.

## Daten {#section-c762bdfe425140d689ea5abf25e9a48a}

Kommagetrennte Liste von IP-Adressen. Jede einzelne Adresse kann ein optionales Suffix &quot;netmask&quot;enthalten, um die Angabe der IP-Adressbereiche zu ermöglichen. See `attribute::ClientAddressFilter` for details.

## Beschreibung {#section-d561b2485e004ef8a2085997d0f4bca6}

Der Zugriff auf diesen Bildkatalog kann auf eine oder mehrere bestimmte Client-IP-Adressen beschränkt werden, indem sie in einem `<addressfilter>` Element angegeben werden. Der Fehler &quot;Anforderung verweigert&quot;wird an den Client zurückgegeben, wenn die Client-IP-Adresse nicht übereinstimmt.

Der Zugriff ist nicht eingeschränkt, wenn `<addressfilter>` er leer oder nicht angegeben ist.

Wenn das Element `<expression>` im `<rule>` Element fehlt oder leer ist, `<addressfilter>` wird es auf alle Anforderungen angewendet.

## Verwandte Themen {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
