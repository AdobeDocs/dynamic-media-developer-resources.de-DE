---
description: Bildanker. Gibt den Verankerungspunkt (Hotspot) einer wiederholbaren Textur, eines Wandrahmens oder eines Dezimalbilds an.
solution: Experience Manager
title: Anker
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# Anker{#anchor}

Bildanker. Gibt den Verankerungspunkt (Hotspot) einer wiederholbaren Textur, eines Wandrahmens oder eines Dezimalbilds an.

Auf ein Vignettenobjekt wird eine wiederholbare Textur angewendet, sodass sich der Texturankerpunkt am Texturankerpunkt des Objekts befindet. Die Herkunft des Objekts ist wiederholbar. Auf ein Vignettenobjekt wird ein Dezimalbild angewendet, sodass sich der dekale Verankerungspunkt am Dezimalpunkt des Objekts befindet. Bei Wandbegrenzungen wird nur der x-Wert verwendet. der y-Wert wird ignoriert.

## Eigenschaften {#section-bc4bc8b897c64535b88681e57d72942f}

Zwei Ganzzahlzahlen, durch Kommas getrennt. Pixel-Versatz relativ zur oberen, linken Ecke des Bildes. Wird ignoriert, wenn `catalog::Alignment=3` und durch feste Farbe und Schrank Materialien.

## Standard {#section-b7ccc419a356415294706cd295ae96c9}

Ist das Feld leer oder nicht vorhanden, wird die obere linke Ecke (0,0) des Bilds für wiederholbare Texturmaterialien verwendet, bzw. bei dekalen Materialien die Mitte des Bilds.

## Verwandte Themen {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[Katalog::Ausrichtung](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [Anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
