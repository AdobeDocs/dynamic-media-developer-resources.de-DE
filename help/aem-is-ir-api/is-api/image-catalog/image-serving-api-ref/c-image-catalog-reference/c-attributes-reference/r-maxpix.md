---
description: Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, die an den Client zurückgegeben werden können.
seo-description: Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, die an den Client zurückgegeben werden können.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

Maximale Antwortbildgröße. Maximale Breite und Höhe des Antwortbilds, die an den Client zurückgegeben werden können.

Der Server gibt einen Fehler zurück, wenn eine Anforderung ein Antwortbild mit einer höheren Breite oder Höhe als `attribute::MaxPix`.

## Eigenschaften {#section-b175425b9e9f48e0b1a71640f6a9e936}

Zwei ganzzahlige Zahlen, größer als 0, durch Kommas getrennt. Breite und Höhe in Pixel. Kann auch so eingestellt sein, dass eine beliebige Größe des Antwortbilds ohne Einschränkungen zulässig `0,0` ist.

## Standard {#section-1003537434da432fb2af100ecdbf9d72}

Vererbt von, `default::MaxPix` wenn nicht definiert oder leer.

## Verwandte Themen {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
