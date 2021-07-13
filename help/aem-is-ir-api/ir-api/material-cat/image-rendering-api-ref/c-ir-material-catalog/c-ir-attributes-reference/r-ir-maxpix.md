---
description: Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, das an den Client zurückgegeben werden kann.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# MaxPix{#maxpix}

Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, das an den Client zurückgegeben werden kann.

Der Server gibt einen Fehler zurück, wenn eine Anfrage zu einem Antwortbild führen würde, dessen Breite und/oder Höhe größer als `attribute::MaxSize` ist.

## Eigenschaften {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Zwei ganze Zahlen, größer als 0, durch Kommas getrennt. Breite und Höhe in Pixel. Kann auch auf 0,0 gesetzt werden, um eine beliebige Größe des Antwortbilds ohne Einschränkungen zuzulassen.

## Standard {#section-45b38dc661854d11b97df5709f4f3434}

Vererbt von Standard::MaxPix , wenn nicht definiert oder wenn leer.

## Verwandte Themen {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
