---
description: Maximale Größe des Antwortbildes. Maximale Breite und Höhe des Antwortbildes, das an den Client zurückgegeben werden kann.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# MaxPix{#maxpix}

Maximale Größe des Antwortbildes. Maximale Breite und Höhe des Antwortbildes, das an den Client zurückgegeben werden kann.

Der Server gibt einen Fehler zurück, wenn eine Anfrage zu einem Antwortbild führen würde, dessen Breite oder Höhe größer als `attribute::MaxPix` ist.

## Eigenschaften {#section-b175425b9e9f48e0b1a71640f6a9e936}

Zwei ganze Zahlen, größer als 0, durch ein Komma getrennt. Breite und Höhe in Pixel. Kann auch auf `0,0` gesetzt werden, um eine beliebige Größe des Antwortbildes ohne Einschränkungen zuzulassen.

## Standard {#section-1003537434da432fb2af100ecdbf9d72}

Von `default::MaxPix` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
