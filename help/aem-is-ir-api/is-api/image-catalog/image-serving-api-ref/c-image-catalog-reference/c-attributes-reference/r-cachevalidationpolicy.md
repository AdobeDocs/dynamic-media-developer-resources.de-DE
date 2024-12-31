---
title: CacheValidationPolicy
description: Validierungsrichtlinie für den Server-Cache. Gibt an, wann Server-seitige Cache-Einträge validiert werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Validierungsrichtlinie für den Server-Cache. Gibt an, wann Server-seitige Cache-Einträge validiert werden.

Bei der ablaufbasierten Validierung werden Quellbilder regelmäßig auf Änderungen überprüft. Bei der katalogbasierten Validierung werden Quellbilder erst überprüft, nachdem der `catalog::TimeStamp` geändert wurde.

Katalogbasierte Validierung wird empfohlen, wenn Bildkataloge verwendet werden. Die Gültigkeitsprüfung sollte verwendet werden, wenn Bilder direkt referenziert werden, ohne dass ein Bildkatalog verwendet wird.

## Eigenschaften {#section-650cbddd81a24c3b8b70479248a45dc9}

Aufzählung. 0 zur Auswahl einer Gültigkeitsprüfung, 1 zur Auswahl einer katalogbasierten Cache-Prüfung.

## Standard {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Von `default::CacheValidationPolicy` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
