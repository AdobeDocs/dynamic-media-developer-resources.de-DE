---
description: Standardzeitstempel für die Bildbearbeitung. Stellt einen Standardwert für den Katalog TimeStamp bereit.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# TimeStamp{#timestamp}

Standardzeitstempel für die Bildbearbeitung. Stellt einen Standardwert für catalog bereit::TimeStamp.

Falls nicht angegeben, verwendet der Server das Änderungsdatum/-zeitpunkt dieser [!DNL *`catalog`*.ini]-Datei.

## Eigenschaften {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datums-/Uhrzeitwert. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* liegt im Bereich von 0 bis 23.

*`zzz`* ist ein 3- oder 4-stelliger Zeitzonen-Code, z. B.  `GMT` oder  `PST`. Die Sommerzeit muss im Zeitzonencode (z. B. `PST` für Pacific Standard Time, vs. `PDT` für Pacific Daylight Savings Time).

*`offset`* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zu GMT. `PDT` entspricht beispielsweise `GMT -7`.

Alle Elemente von String formatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen wird der Änderungszeitpunkt der Datei [!DNL *`catalog`*.ini] verwendet.

## Standard {#section-ac465313c97943ed97d41ea852329177}

Wenn leer oder nicht definiert, verwendet der Server die Dateiänderungszeit dieser `*`catalog`*.ini`-Datei.

## Verwandte Themen {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
