---
description: Auflösung. Die „reale“ Bildauflösung wird in der Regel als Pixel pro Zoll ausgedrückt, kann aber auch in anderen Einheiten verwendet werden, z. B. Pixel pro Meter.
solution: Experience Manager
title: Auflösung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# Auflösung{#resolution}

Auflösung. Die „reale“ Bildauflösung wird in der Regel als Pixel pro Zoll ausgedrückt, kann aber auch in anderen Einheiten verwendet werden, z. B. Pixel pro Meter.

## Eigenschaften {#section-985ca2ad858c4e9c9cbb303f55447553}

Reelle Zahl, größer als 0. Erforderlich für Textur- und Abziehbildmaterialien, es sei denn, die Bildauflösung entspricht dem Attribut::Resolution. Wird von einfarbigen und Schrankmaterialien ignoriert.

## Standard {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` wird verwendet, wenn das Feld nicht vorhanden ist, der Wert 0 oder negativ ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
