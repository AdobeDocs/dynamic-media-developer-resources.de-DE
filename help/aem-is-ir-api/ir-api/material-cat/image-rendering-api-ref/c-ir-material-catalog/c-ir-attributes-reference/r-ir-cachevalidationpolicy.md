---
description: Validierungsrichtlinie für den Server-Cache Gibt an, wann serverseitige Cache-Einträge validiert werden.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Validierungsrichtlinie für den Server-Cache Gibt an, wann serverseitige Cache-Einträge validiert werden.

Bei der ablaufbasierten Validierung werden Quellmaterialien und Vignetten regelmäßig überprüft, ob sie sich geändert haben. Bei katalogbasierter Validierung werden Quellbilder erst überprüft, nachdem der Wert `catalog::TimeStamp` geändert wurde.

Katalogbasierte Validierung wird empfohlen, wenn sowohl Material- als auch Vignettenkataloge verwendet werden. Eine ablaufbasierte Validierung sollte verwendet werden, wenn in Image Rendering-Anforderungen direkt über den Pfad auf Vignetten verwiesen wird.

## Eigenschaften {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 zur Auswahl der ablaufbasierten Validierung. 1 zur Auswahl der Katalogbasierten Cache-Validierung.

## Standard {#section-e09f3af8b6b3497d963199988dc5345d}

Vererbt von `default::CacheValidationPolicy`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-b374e4d908e24af8995b2b376ca1be8b}

[Katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
