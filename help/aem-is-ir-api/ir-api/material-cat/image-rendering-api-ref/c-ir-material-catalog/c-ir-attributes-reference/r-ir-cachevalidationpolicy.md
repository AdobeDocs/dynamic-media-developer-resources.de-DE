---
title: CacheValidationPolicy
description: Validierungsrichtlinie für den Server-Cache. Gibt an, wann Server-seitige Cache-Einträge validiert werden.
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

Validierungsrichtlinie für den Server-Cache. Gibt an, wann Server-seitige Cache-Einträge validiert werden.

Bei der Gültigkeitsprüfung werden Quellmaterialien und Vignetten regelmäßig überprüft, um festzustellen, ob sie sich geändert haben. Bei der katalogbasierten Validierung werden Quellbilder erst überprüft, nachdem der `catalog::TimeStamp` geändert wurde.

Katalogbasierte Validierung wird empfohlen, wenn sowohl Material- als auch Vignettenkataloge verwendet werden. Gültigkeits-basierte Validierung sollte verwendet werden, wenn in Bild-Rendering-Anfragen direkt über den Pfad auf Vignetten verwiesen wird.

## Eigenschaften {#section-46e13cb341eb442c86e0d8292de23ea0}

Aufzählung. 0, um die ablaufbasierte Validierung auszuwählen. 1, um die katalogbasierte Cache-Validierung auszuwählen.

## Standard {#section-e09f3af8b6b3497d963199988dc5345d}

Von `default::CacheValidationPolicy` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
