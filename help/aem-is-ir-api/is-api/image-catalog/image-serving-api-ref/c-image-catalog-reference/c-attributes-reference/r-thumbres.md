---
description: Standardauflösung für Miniaturansichten. Stellt eine Standardeinstellung für die Auflösung des Miniaturansichtsobjekts bereit, falls ein bestimmter Katalogdatensatz keinen gültigen ThumbRes-Katalogwert enthält.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# ThumbRes{#thumbres}

Standardauflösung für Miniaturansichten. Stellt eine Standardeinstellung für die Auflösung des Miniaturansichtsobjekts bereit, falls ein bestimmter Katalogdatensatz keinen gültigen Katalogwert enthält::ThumbRes -Wert.

Wird nur für Miniaturansichten ( `req=tmb`) und `catalog::ThumbType=3` verwendet.

## Eigenschaften {#section-88d37d0e030f4879a9e584dd2cc780f3}

Die tatsächliche Zahl, die größer als 0,0 ist, normalerweise in Pixel pro Zoll ausgedrückt, kann aber auch in anderen Einheiten wie Pixeln pro Meter enthalten sein.

## Standard {#section-86588899ec9b4276a98b03d7faf64003}

Wird von `default::ThumbRes` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
