---
description: Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, die an den Client zurückgegeben werden können.
seo-description: Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, die an den Client zurückgegeben werden können.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# MaxPix{#maxpix}

Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, die an den Client zurückgegeben werden können.

Der Server gibt einen Fehler zurück, wenn eine Anforderung zu einem Antwortbild führen würde, dessen Breite und/oder Höhe größer als `attribute::MaxSize` ist.

## Eigenschaften {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Zwei ganzzahlige Zahlen, größer als 0, durch Kommas getrennt. Breite und Höhe in Pixel. Kann auch auf 0,0 gesetzt werden, um eine beliebige Größe des Antwortbilds ohne Einschränkungen zuzulassen.

## Standard {#section-45b38dc661854d11b97df5709f4f3434}

Von Standard übernommen::MaxPix, wenn nicht definiert oder leer.

## Verwandte Themen {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
