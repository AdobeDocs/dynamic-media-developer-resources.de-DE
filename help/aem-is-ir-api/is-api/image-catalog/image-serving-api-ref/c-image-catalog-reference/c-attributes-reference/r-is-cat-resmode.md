---
description: Standard-Resamplingmodus. Gibt die standardmäßigen Attribute für Neuberechnung und Interpolation an, die für die Skalierung von Bilddaten verwendet werden.
seo-description: Standard-Resamplingmodus. Gibt die standardmäßigen Attribute für Neuberechnung und Interpolation an, die für die Skalierung von Bilddaten verwendet werden.
seo-title: ResMode
solution: Experience Manager
title: ResMode
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# ResMode{#resmode}

Standard-Resamplingmodus. Gibt die standardmäßigen Attribute für Neuberechnung und Interpolation an, die für die Skalierung von Bilddaten verwendet werden.

Wird verwendet, wenn `resMode=` in einer Anforderung nicht angegeben ist.

## Eigenschaften {#section-493f900be522486f97710cebdc4460c2}

Enum. Legen Sie für `bilin`, 3 für `bicub` oder 4 für `sharp2`-Interpolationsmodus fest (weitere Informationen finden Sie unter ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`). `sharp` (1) nicht mehr unterstützt wird. Verwenden Sie für optimale Ergebnisse `sharp2` (4).

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Vererbt von `default::ResMode`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
