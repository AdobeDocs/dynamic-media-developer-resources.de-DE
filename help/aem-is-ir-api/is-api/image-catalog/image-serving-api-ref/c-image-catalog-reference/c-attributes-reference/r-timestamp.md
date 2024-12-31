---
title: Zeitstempel
description: Zeitstempel der Standardbildänderung. Es stellt einen Standardwert für den Katalog-Zeitstempel bereit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Zeitstempel{#timestamp}

Zeitstempel der Standardbildänderung. Stellt einen Standardwert für „catalog:TimeStamp“ bereit.

Wenn nicht anders angegeben, verwendet der Server das Änderungsdatum/die Änderungsuhrzeit dieser Datei [!DNL *`catalog`*.ini].

## Eigenschaften {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datums-/Uhrzeitwert Dies kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert in einem der folgenden Formate sein:

Der Datums-/Uhrzeitwert *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

Der Datums-/Uhrzeitwert *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

Der Zeitwert *`hh`* liegt im Bereich von 0 bis 23.

Der Zeitwert *`zzz`* ist ein drei- oder vierstelliger Zeitzonencode, z. B. `GMT` oder `PST`. Die Sommerzeit muss im Zeitzonen-Code berücksichtigt werden (z. B. `PST` für Pacific Standard Time oder `PDT` für Pacific Daylight Savings Time).

Der Zeitwert *`offset`* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten, relativ zu GMT. `PDT` entspricht beispielsweise `GMT -7`.

Alle Elemente von zeichenfolgenformatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *`catalog`*.ini] verwendet.

## Standard {#section-ac465313c97943ed97d41ea852329177}

Wenn leer oder nicht definiert, verwendet der Server die Dateiänderungszeit dieser Datei `*`Katalog`*.ini`.

## Verwandte Themen {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
