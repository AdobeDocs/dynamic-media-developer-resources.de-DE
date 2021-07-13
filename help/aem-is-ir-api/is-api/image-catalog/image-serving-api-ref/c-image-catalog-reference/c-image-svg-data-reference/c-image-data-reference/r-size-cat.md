---
description: Bildgröße. Die Pixelgröße des Bildes in voller Auflösung, auf das vom Katalogpfad verwiesen wird.
solution: Experience Manager
title: Größe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# Größe{#size}

Bildgröße. Die Pixelgröße des von catalog::Path referenzierten Bildes in voller Auflösung.

Wenn dieser Wert angegeben wird, verwendet Image Serving ihn, um zu vermeiden, dass das Bild geöffnet werden muss, um die tatsächliche Bildgröße zu erhalten.

>[!NOTE]
>
>Wenn `catalog::Size`angegeben ist und nicht mit der tatsächlichen Bildgröße in voller Auflösung übereinstimmt, kann dies zu undefiniertem Verhalten führen.

## Eigenschaften {#section-5c914ec8b1444a8e99d811b647cd42a3}

Zwei ganzzahlige Zahlen, jeweils größer 0, durch Kommas getrennt. Optional.

## Standard {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Wenn das Feld nicht vorhanden ist oder das Feld leer ist, wird die tatsächliche Bildgröße verwendet.

## Verwandte Themen {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
