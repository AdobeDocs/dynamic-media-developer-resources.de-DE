---
description: Standard-Resamplingmodus. Gibt die standardmäßigen Attribute für Neuberechnung und Interpolation an, die für die Skalierung von Bilddaten verwendet werden.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

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
