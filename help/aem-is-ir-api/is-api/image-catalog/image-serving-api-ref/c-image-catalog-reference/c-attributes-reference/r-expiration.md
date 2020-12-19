---
description: Standardmäßige Clientcache-Zeit bis zum Live-Betrieb. Bietet ein Standard-Ablaufintervall, falls ein bestimmter Katalogeintrag keinen gültigen Katalogablaufwert enthält.
seo-description: Standardmäßige Clientcache-Zeit bis zum Live-Betrieb. Bietet ein Standard-Ablaufintervall, falls ein bestimmter Katalogeintrag keinen gültigen Katalogablaufwert enthält.
seo-title: Ablauf
solution: Experience Manager
title: Ablauf
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 4%

---


# Ablauf{#expiration}

Standardmäßige Clientcache-Zeit bis zum Live-Betrieb. Bietet ein Standardablaufintervall, falls ein bestimmter Katalogeintrag keinen gültigen Katalog enthält::Expiration-Wert.

## Eigenschaften {#section-063be3b2f13a48a3a5ab8080718e9812}

Reale Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung der Antwortdaten. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Zwischenspeicherung des Clients effektiv deaktiviert wird. Auf -1 setzen, um als `never expire` zu markieren.

## Standard {#section-f55308b195c04083996f6717c8537634}

Vererbt von `default::Expiration`, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer, bevor der Cache abläuft. Die Standard-TTL beträgt 10 Stunden.

## Verwandte Themen {#section-b2411d99ddb14115ad475d506efd8967}

[Katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [Attribut::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [Attribut::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
