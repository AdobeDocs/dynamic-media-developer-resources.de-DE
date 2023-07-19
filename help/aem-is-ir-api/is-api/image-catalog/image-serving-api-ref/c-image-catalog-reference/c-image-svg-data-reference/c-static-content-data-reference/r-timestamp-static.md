---
title: TimeStamp
description: Wenn `attribute::UseLastModified` festgelegt ist, wird der Wert "catalog::TimeStamp"in der HTTP-Antwort als HTTP-Header mit der Bezeichnung "Last-Modified"zurückgegeben. Die Kopfzeile "Last-Modified"wird immer für statische Inhalte zurückgegeben, auch wenn `attribute::UseLastModified` nicht festgelegt ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Wenn `attribute::UseLastModified` festgelegt ist, wird die `catalog::TimeStamp` -Wert in der HTTP-Antwort als HTTP-Header mit der letzten Änderung zurückgegeben. Die Kopfzeile &quot;Zuletzt geändert&quot;wird immer für statische Inhalte zurückgegeben, auch wenn `attribute::UseLastModified` nicht festgelegt ist.

Für Bild- und SVG-Inhalte, `catalog::TimeStamp` wird auch für die Katalogbasierte Cache-Validierung verwendet (siehe [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Eigenschaften {#section-2298a384b5cb43929542655c5a49beb2}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* liegt im Bereich von 0 bis 23.

*`zzz`* ist ein aus drei oder vier Zeichen bestehender Zeitzonen-Code, z. B. &quot;GMT&quot;oder &quot;PST&quot;. Berücksichtigen Sie die Sommerzeit im Zeitzonencode. Beispielsweise &quot;PST&quot;für die Pacific Standard-Zeit im Vergleich zu &quot;PDT&quot;für die Sommerzeit (Pacific Daylight Savings Time).

*`offset`* ist ein Zeitzonenversatz in Stunden oder `hours:minutes`, relativ zu GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente von String formatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und der Änderungszeitpunkt des `*`Katalog`*.ini` wird stattdessen verwendet.

## Standard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` wenn das Feld leer ist oder nicht vorhanden ist.

## Verwandte Themen {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
