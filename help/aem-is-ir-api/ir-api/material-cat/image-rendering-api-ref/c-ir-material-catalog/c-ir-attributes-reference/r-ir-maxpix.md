---
title: MaxPix
description: Maximale Größe des Antwortbildes. Maximale Breite und Höhe des Antwortbildes, das an den Client zurückgegeben werden kann.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# MaxPix{#maxpix}

Maximale Größe des Antwortbildes. Maximale Breite und Höhe des Antwortbildes, das an den Client zurückgegeben werden kann.

Der Server gibt einen Fehler zurück, wenn eine Anfrage zu einem Antwortbild führen würde, dessen Breite und/oder Höhe größer als `attribute::MaxSize` ist.

## Eigenschaften {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Zwei ganze Zahlen, größer als 0, durch ein Komma getrennt. Breite und Höhe in Pixel. Kann auch auf 0,0 gesetzt werden, um eine beliebige Antwortbildgröße ohne Einschränkungen zu ermöglichen.

## Standard {#section-45b38dc661854d11b97df5709f4f3434}

Von default::MaxPix geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
