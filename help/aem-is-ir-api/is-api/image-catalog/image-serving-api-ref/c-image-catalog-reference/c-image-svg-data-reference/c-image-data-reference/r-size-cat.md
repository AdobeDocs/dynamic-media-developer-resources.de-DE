---
description: Bildgröße. Die Pixelgröße des Bildes mit voller Auflösung, auf das vom Katalogpfad verwiesen wird.
seo-description: Bildgröße. Die Pixelgröße des Bildes mit voller Auflösung, auf das vom Katalogpfad verwiesen wird.
seo-title: Größe
solution: Experience Manager
title: Größe
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Größe{#size}

Bildgröße. Die Pixelgröße des Bildes mit voller Auflösung, auf das vom Katalog verwiesen wird::Path.

Wenn dieser Wert angegeben ist, verwendet Image Serving ihn, um zu vermeiden, dass das Bild geöffnet werden muss, um die tatsächliche Bildgröße zu erhalten.

>[!NOTE]
>
>Wenn `catalog::Size`eine Bildgröße angegeben wird, die nicht mit der tatsächlichen Bildgröße in voller Auflösung übereinstimmt, kann dies zu einem nicht definierten Verhalten führen.

## Eigenschaften {#section-5c914ec8b1444a8e99d811b647cd42a3}

Zwei Ganzzahlzahlen, jeweils größer als 0, durch Kommas getrennt. Optional.

## Standard {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Wenn das Feld nicht vorhanden ist oder das Feld leer ist, wird die tatsächliche Größe des Bildes verwendet.

## Verwandte Themen {#section-e63797357d5a4119a10db1e6e088f6e9}

[Katalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
