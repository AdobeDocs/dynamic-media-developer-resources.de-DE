---
description: Validierungsrichtlinie für den Server-Cache Gibt an, wann serverseitige Cache-Einträge validiert werden.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Validierungsrichtlinie für den Server-Cache Gibt an, wann serverseitige Cache-Einträge validiert werden.

Bei der ablaufbasierten Validierung werden Quellbilder regelmäßig überprüft, ob sie sich geändert haben. Bei katalogbasierter Validierung werden Quellbilder erst überprüft, nachdem der Wert `catalog::TimeStamp` geändert wurde.

Eine katalogbasierte Validierung wird empfohlen, wenn Bildkataloge verwendet werden. Eine ablaufbasierte Validierung sollte verwendet werden, wenn direkt auf Bilder verwiesen wird, ohne dass ein Bildkatalog verwendet wird.

## Eigenschaften {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 zur Auswahl der ablaufbasierten Validierung, 1 zur Auswahl der katalogbasierten Cache-Validierung.

## Standard {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Vererbt von `default::CacheValidationPolicy`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-a0c922fa519641f2bce05e75e4eb51d0}

[Katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
