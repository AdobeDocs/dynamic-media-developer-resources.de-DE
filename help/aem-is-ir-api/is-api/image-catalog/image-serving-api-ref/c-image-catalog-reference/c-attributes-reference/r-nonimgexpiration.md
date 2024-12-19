---
description: Client-Cache-TTL für Nicht-Bildantworten. Stellt das Ablaufintervall für bestimmte Nicht-Bildantworten bereit.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

Client-Cache-TTL für Nicht-Bildantworten. Stellt das Ablaufintervall für bestimmte Nicht-Bildantworten bereit.

Stellt das Ablaufintervall für bestimmte Nicht-Bildantworten bereit, einschließlich der Antworten, die als Antwort auf die folgenden Befehle gesendet werden:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Eigenschaften {#section-d37e3113f4b1468b86b5a14e80d94c83}

Reelle Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf der Gültigkeit seit Generierung der Antwortdaten. Auf 0 gesetzt, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Client-Zwischenspeicherung für standardmäßige Bildantworten effektiv deaktiviert wird. Legen Sie ihn auf -1 fest, um dies als &quot;*läuft nie ab* zu kennzeichnen.

## Standard {#section-96981360c0234b7f824d2ff7c25a7954}

Von `default::NonImgExpiration` geerbt, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer vor Ablauf des Cache. Die Standard-TTL beträgt 6 Minuten.

## Verwandte Themen {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
