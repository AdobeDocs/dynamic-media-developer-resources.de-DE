---
description: Standard-Zeitstempel für die Bildänderung. Stellt einen Standardwert für den Katalog TimeStamp bereit.
seo-description: Standard-Zeitstempel für die Bildänderung. Stellt einen Standardwert für den Katalog TimeStamp bereit.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Standard-Zeitstempel für die Bildänderung. Stellt einen Standardwert für catalog::TimeStamp bereit.

Wenn nicht angegeben, verwendet der Server das Änderungsdatum/-zeitpunkt dieser [!DNL *`catalog`*.ini]-Datei.

## Eigenschaften {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datums-/Uhrzeitwert. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* liegt im Bereich von 0 bis 23.

*`zzz`* ist ein 3- oder 4-Zeichen-Zeitzonencode, z. B.  `GMT` oder  `PST`. Die Sommerzeit muss im Zeitzonencode (z.B. `PST` für Pacific Standard Time und `PDT` für Pacific Daylight Savings Time).

*`offset`* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zum GMT. `PDT` entspricht beispielsweise `GMT -7`.

Alle Elemente der String-formatierten Datums-/Uhrzeitwerte müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *`catalog`*.ini] verwendet.

## Standard {#section-ac465313c97943ed97d41ea852329177}

Wenn leer oder nicht definiert, verwendet der Server die Dateiänderungszeit dieser ` *`catalog`*.ini`-Datei.

## Verwandte Themen {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[Katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [Attribut::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [Attribut::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
