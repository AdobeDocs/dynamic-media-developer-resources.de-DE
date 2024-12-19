---
description: Standardauflösung für Miniaturen. Bietet einen Standard für die Objektauflösung für Miniaturansichten für den Fall, dass ein bestimmter Katalogdatensatz keinen gültigen ThumbRes-Katalogwert enthält.
solution: Experience Manager
title: Daumenabdruck
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# Daumenabdruck{#thumbres}

Standardauflösung für Miniaturen. Bietet einen Standard für die Objektauflösung für Miniaturansichten, falls ein bestimmter Katalogeintrag keinen gültigen Wert für catalog:ThumbRes enthält.

Wird nur für Anfragen von Miniaturansichten (`req=tmb`) und bei der `catalog::ThumbType=3` verwendet.

## Eigenschaften {#section-88d37d0e030f4879a9e584dd2cc780f3}

Reelle Zahl, größer als 0.Typischerweise ausgedrückt als Pixel pro Zoll, kann aber auch in anderen Einheiten wie Pixel pro Meter enthalten sein.

## Standard {#section-86588899ec9b4276a98b03d7faf64003}

Von `default::ThumbRes` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog:ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
