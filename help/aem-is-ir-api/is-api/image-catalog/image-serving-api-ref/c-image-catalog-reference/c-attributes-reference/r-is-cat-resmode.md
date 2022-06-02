---
title: ResMode
description: Standardmäßiger Resamplingmodus. Gibt die standardmäßigen Resampling- und Interpolationsattribute an, die für die Skalierung von Bilddaten verwendet werden sollen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# ResMode{#resmode}

Standardmäßiger Resamplingmodus. Gibt die standardmäßigen Resampling- und Interpolationsattribute an, die für die Skalierung von Bilddaten verwendet werden sollen.

Wird verwendet, wenn `resMode=` in einer Anfrage nicht angegeben ist.

## Eigenschaften {#section-493f900be522486f97710cebdc4460c2}

Enum. Auf 2 setzen für `bilin`, 3 für `bicub`oder 4 für `sharp2` Interpolationsmodus (siehe [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) für Details). `sharp` (1) wird nicht mehr unterstützt. Verwendung `sharp2` (4), um die besten Ergebnisse zu erzielen.

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Vererbt von `default::ResMode` wenn nicht definiert oder leer ist.

## Verwandte Themen {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
