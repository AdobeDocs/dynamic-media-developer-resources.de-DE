---
description: Client-Cache-TTL für Standard-Bildantworten. Stellt das Ablaufintervall für Standard-Bildantworten bereit (Antworten, die ein Standardbild zurückgeben, das mit defaultImage= oder attribute DefaultImage angegeben wurde).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

Client-Cache-TTL für Standard-Bildantworten. Stellt das Ablaufintervall für Standard-Bildantworten bereit (Antworten, die ein Standardbild zurückgeben, das mit defaultImage= oder attribute::DefaultImage angegeben wurde).

Wird nur angewendet, wenn das Standardbild nicht mit einem Katalogdatensatz verknüpft ist oder wenn der Standardbildkatalogdatensatz keinen bestimmten `catalog::Expiration`-Wert bereitstellt.

## Eigenschaften {#section-e564512476604fd7b964f9f2903d6d33}

Reale Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung der Antwortdaten. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Client-Zwischenspeicherung für Standard-Bildantworten deaktiviert wird. Auf `-1` setzen, um als `never expire` zu markieren.

## Standard {#section-131cd32c2e214391857dba5af321f8cd}

Vererbt von `default::DefaultExpiration`, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer, bevor der Cache abläuft. Die Standard-TTL ist 1 Stunde.

## Verwandte Themen {#section-d8642c22e3d947129367dd76366963d6}

[Katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
