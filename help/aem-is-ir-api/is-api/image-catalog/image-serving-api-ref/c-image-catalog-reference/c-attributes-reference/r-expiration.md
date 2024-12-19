---
description: Standardmäßige Gültigkeitsdauer des Client-Cache. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogeintrag keinen gültigen Katalog-Ablaufwert enthält.
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# Ablauf{#expiration}

Standardmäßige Gültigkeitsdauer des Client-Cache. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogeintrag keinen gültigen Wert für catalog:expiration enthält.

## Eigenschaften {#section-063be3b2f13a48a3a5ab8080718e9812}

Reelle Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf der Gültigkeit seit Generierung der Antwortdaten. Auf 0 gesetzt, um das Antwortbild immer sofort ablaufen zu lassen, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 gesetzt, um als `never expire` zu markieren.

## Standard {#section-f55308b195c04083996f6717c8537634}

Von `default::Expiration` geerbt, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer vor Ablauf des Cache. Die Standard-TTL beträgt 10 Stunden.

## Verwandte Themen {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
