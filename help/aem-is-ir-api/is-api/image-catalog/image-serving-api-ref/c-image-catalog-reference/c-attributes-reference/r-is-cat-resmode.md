---
title: ResMode
description: Standard-Resampling-Modus. Gibt die standardmäßigen Resampling- und Interpolationsattribute an, die für die Skalierung von Bilddaten verwendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
TQID: 'https://experienceleague.adobe.com/jYteRal6Z6ea7AWTuoGA9KFDAyPS1rV7t-KzZBbm-s0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 3%

---

# ResMode{#resmode}

Standard-Resampling-Modus. Gibt die standardmäßigen Resampling- und Interpolationsattribute an, die für die Skalierung von Bilddaten verwendet werden.

Wird verwendet, wenn `resMode=` in einer Anfrage nicht angegeben wird.

## Eigenschaften {#section-493f900be522486f97710cebdc4460c2}

Aufzählung. Festlegung auf 2 für `bilin`, 3 für `bicub` oder 4 für `sharp2` Interpolationsmodus (Einzelheiten siehe [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md)). `sharp` (1) wird nicht mehr unterstützt. Verwenden Sie stattdessen `sharp2` (4), um optimale Ergebnisse zu erzielen.

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Von `default::ResMode` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
