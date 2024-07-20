---
description: Lösung. Bildauflösung "Echtzeit", die normalerweise in Pixel pro Zoll ausgedrückt wird, aber auch in anderen Einheiten wie Pixeln pro Meter enthalten sein kann.
solution: Experience Manager
title: Auflösung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# Auflösung{#resolution}

Lösung. Bildauflösung &quot;Echtzeit&quot;, die normalerweise in Pixel pro Zoll ausgedrückt wird, aber auch in anderen Einheiten wie Pixeln pro Meter enthalten sein kann.

## Eigenschaften {#section-985ca2ad858c4e9c9cbb303f55447553}

Real Zahl, größer als 0. Erforderlich für Textur- und Dekormaterialien, es sei denn, die Bildauflösung ist mit der des Attributs::Resolution identisch. Ignoriert durch feste Farbe und Möbel.

## Standard {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert 0 oder negativ ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
