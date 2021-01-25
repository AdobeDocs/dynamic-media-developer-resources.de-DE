---
description: Client-Cache-TTL für Nicht-Bild-Antworten. Stellt das Ablaufintervall für bestimmte nicht bildbezogene Antworten bereit.
seo-description: Client-Cache-TTL für Nicht-Bild-Antworten. Stellt das Ablaufintervall für bestimmte nicht bildbezogene Antworten bereit.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# NonImgExpiration{#nonimgexpiration}

Client-Cache-TTL für Nicht-Bild-Antworten. Stellt das Ablaufintervall für bestimmte nicht bildbezogene Antworten bereit.

Stellt das Ablaufintervall für bestimmte nicht bildbezogene Antworten bereit, einschließlich solcher, die als Antwort auf die folgenden Befehle gesendet werden:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Eigenschaften {#section-d37e3113f4b1468b86b5a14e80d94c83}

Reale Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung der Antwortdaten. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Client-Zwischenspeicherung für Standard-Bildantworten deaktiviert wird. Auf -1 setzen, um als *nie ablaufen* zu markieren.

## Standard {#section-96981360c0234b7f824d2ff7c25a7954}

Vererbt von `default::NonImgExpiration`, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer, bevor der Cache abläuft. Die Standard-TTL beträgt 6 Minuten.

## Verwandte Themen {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[Katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
