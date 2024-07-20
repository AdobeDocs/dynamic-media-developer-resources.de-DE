---
description: Standardmäßige Client-Cache-Zeit für die Live-Schaltung. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogdatensatz keinen gültigen Katalogablaufwert enthält.
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

Standardmäßige Client-Cache-Zeit für die Live-Schaltung. Bietet ein standardmäßiges Ablaufintervall, falls ein bestimmter Katalogdatensatz keinen gültigen Katalogwert enthält::Expiration -Wert.

## Eigenschaften {#section-063be3b2f13a48a3a5ab8080718e9812}

Real number, 0 oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung der Antwortdaten. Auf 0 setzen, damit das Antwortbild immer sofort abläuft, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 setzen, um als `never expire` zu markieren.

## Standard {#section-f55308b195c04083996f6717c8537634}

Wird von `default::Expiration` übernommen, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer, bevor der Cache abläuft. Die standardmäßige TTL beträgt 10 Stunden.

## Verwandte Themen {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
