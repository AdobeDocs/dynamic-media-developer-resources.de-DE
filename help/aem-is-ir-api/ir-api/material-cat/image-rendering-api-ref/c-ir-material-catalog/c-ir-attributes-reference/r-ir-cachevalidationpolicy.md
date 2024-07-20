---
title: CacheValidationPolicy
description: Validierungsrichtlinie für Server-Cache. Gibt an, wann serverseitige Cache-Einträge validiert werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Validierungsrichtlinie für Server-Cache. Gibt an, wann serverseitige Cache-Einträge validiert werden.

Bei der ablaufbasierten Validierung werden Quellmaterialien und Vignetten regelmäßig überprüft, um festzustellen, ob sie sich geändert haben. Bei katalogbasierter Validierung werden Quellbilder erst überprüft, nachdem der `catalog::TimeStamp` -Wert geändert wurde.

Eine Catalog-basierte Validierung wird empfohlen, wenn sowohl Material- als auch Vignettenkataloge verwendet werden. Eine ablaufbasierte Validierung sollte verwendet werden, wenn in Bildwiedergabe-Anforderungen direkt über den Pfad auf Vignetten verwiesen wird.

## Eigenschaften {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 zum Auswählen einer ablaufbasierten Validierung. 1 zur Auswahl der Katalogbasierten Cache-Validierung.

## Standard {#section-e09f3af8b6b3497d963199988dc5345d}

Wird von `default::CacheValidationPolicy` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
