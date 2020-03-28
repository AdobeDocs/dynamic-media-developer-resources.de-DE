---
description: Client-Cache-TTL für Standard-Bildantworten. Stellt das Ablaufintervall für Standard-Bildantworten bereit (Antworten, die ein Standardbild zurückgeben, das mit defaultImage= oder attribute DefaultImage angegeben wurde).
seo-description: Client-Cache-TTL für Standard-Bildantworten. Stellt das Ablaufintervall für Standard-Bildantworten bereit (Antworten, die ein Standardbild zurückgeben, das mit defaultImage= oder attribute DefaultImage angegeben wurde).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultExpiration{#defaultexpiration}

Client-Cache-TTL für Standard-Bildantworten. Stellt das Ablaufintervall für Standard-Bildantworten bereit (Antworten, die ein Standardbild zurückgeben, das mit defaultImage= oder attribute::DefaultImage angegeben wurde).

Wird nur angewendet, wenn das Standardbild nicht mit einem Katalogdatensatz verknüpft ist oder wenn der Standardbildkatalogdatensatz keinen bestimmten `catalog::Expiration` Wert bereitstellt.

## Eigenschaften {#section-e564512476604fd7b964f9f2903d6d33}

Real number, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung der Antwortdaten. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Client-Zwischenspeicherung für Standard-Bildantworten deaktiviert wird. Auf `-1` Markieren als `never expire`.

## Standard {#section-131cd32c2e214391857dba5af321f8cd}

Vererbt von, `default::DefaultExpiration` wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer, bevor der Cache abläuft. Die Standard-TTL ist 1 Stunde.

## Verwandte Themen {#section-d8642c22e3d947129367dd76366963d6}

[Katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
