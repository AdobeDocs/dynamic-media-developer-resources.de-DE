---
description: Standardmäßiger Resamplingmodus. Gibt die standardmäßigen Resampling- und Interpolationsattribute an, die für die Skalierung von Bilddaten verwendet werden sollen.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

Standardmäßiger Resamplingmodus. Gibt die standardmäßigen Resampling- und Interpolationsattribute an, die für die Skalierung von Bilddaten verwendet werden sollen.

Wird verwendet, wenn `resMode=` in einer Anforderung nicht angegeben ist.

## Eigenschaften {#section-493f900be522486f97710cebdc4460c2}

Enum. Legen Sie 2 für `bilin`, 3 für `bicub` oder 4 für `sharp2` Interpolationsmodus fest (weitere Informationen finden Sie unter ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`). `sharp` (1) wird nicht mehr unterstützt. Verwenden Sie stattdessen `sharp2` (4) , um die besten Ergebnisse zu erzielen.

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Wird von `default::ResMode` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
