---
title: Zeitstempel
description: Zeitstempel der Standardbildänderung. Es stellt einen Standardwert für den Katalog-Zeitstempel bereit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
TQID: 'https://experienceleague.adobe.com/Wyj0OJrb0URsXaymXmx1aB82Qyxun1HatBUqBS4F6cE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
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

Der Zeitwert *`offset`* ist ein Zeitzonenversatz in Stunden oder Stunden:minutes relativ zum GMT. `PDT` entspricht beispielsweise `GMT -7`.

Alle Elemente von zeichenfolgenformatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *`catalog`*.ini] verwendet.

## Standard {#section-ac465313c97943ed97d41ea852329177}

Wenn leer oder nicht definiert, verwendet der Server die Dateiänderungszeit dieser Datei `*`Katalog`*.ini`.

## Verwandte Themen {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
