---
description: Client-Cache-TTL für Nicht-Bild-Antworten. Bietet das Ablaufintervall für bestimmte Nicht-Bild-Antworten.
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

Client-Cache-TTL für Nicht-Bild-Antworten. Bietet das Ablaufintervall für bestimmte Nicht-Bild-Antworten.

Bietet das Ablaufintervall für bestimmte Nicht-Bild-Antworten, einschließlich der Antworten auf die folgenden Befehle:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Eigenschaften {#section-d37e3113f4b1468b86b5a14e80d94c83}

Real number, 0 oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung der Antwortdaten. Auf 0 setzen, damit das Antwortbild immer sofort abläuft, wodurch das Client-Caching für standardmäßige Bildantworten effektiv deaktiviert wird. Auf -1 setzen, um als *niemals abläuft* zu markieren.

## Standard {#section-96981360c0234b7f824d2ff7c25a7954}

Wird von `default::NonImgExpiration` übernommen, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer, bevor der Cache abläuft. Die standardmäßige TTL beträgt 6 Minuten.

## Verwandte Themen {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
