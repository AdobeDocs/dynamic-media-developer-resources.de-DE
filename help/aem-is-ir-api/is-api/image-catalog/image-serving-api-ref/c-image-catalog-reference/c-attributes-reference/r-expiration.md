---
description: Standardmäßige Gültigkeitsdauer des Client-Cache. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogeintrag keinen gültigen Katalog-Ablaufwert enthält.
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
TQID: 'https://experienceleague.adobe.com/NkQ-Bj-gHGksaD4Tmt7k8fYVEYfe67ACo4oWS25dKOE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
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
