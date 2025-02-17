---
description: Bildanker. Gibt den Ankerpunkt (Hotspot) eines wiederholbaren Textur-, Wand- oder Abziehbilds an.
solution: Experience Manager
title: Anker
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# Anker{#anchor}

Bildanker. Gibt den Ankerpunkt (Hotspot) eines wiederholbaren Textur-, Wand- oder Abziehbilds an.

Eine wiederholbare Textur wird auf ein Vignettenobjekt angewendet, sodass sich der Texturankerpunkt am Texturursprungspunkt des Objekts befindet. Ein Abziehbild wird auf ein Vignettenobjekt angewendet, sodass sich der Abziehbildankerpunkt am Abziehbildursprungspunkt des Objekts befindet. Für Wandränder wird nur der Wert „x“ verwendet; der Wert „y“ wird ignoriert.

## Eigenschaften {#section-bc4bc8b897c64535b88681e57d72942f}

Zwei ganze Zahlen, durch ein Komma getrennt. Pixel-Versatz relativ zur oberen linken Ecke des Bildes. Wird ignoriert, wenn `catalog::Alignment=3` und durch einfarbige Materialien und Schränke.

## Standard {#section-b7ccc419a356415294706cd295ae96c9}

Wenn das Feld leer oder nicht vorhanden ist, wird die obere linke Ecke (0,0) des Bildes für wiederholbare Texturmaterialien oder die Mitte des Bildes bei Abziehmaterialien verwendet.

## Verwandte Themen {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::align](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
