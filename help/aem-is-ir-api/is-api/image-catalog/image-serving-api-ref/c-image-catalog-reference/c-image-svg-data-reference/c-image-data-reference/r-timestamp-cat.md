---
description: 'null'
seo-description: 'null'
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 3148cc25-3b9a-499a-b0da-1ebe9ae99f69
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---


# TimeStamp{#timestamp}

Wenn `attribute::UseLastModified` eingestellt ist, wird der Wert `catalog::TimeStamp` in der HTTP-Antwort als Last-Modified HTTP-Header zurückgegeben. Die Kopfzeile &quot;Zuletzt geändert&quot;wird immer für statische Inhalte zurückgegeben, auch wenn `attribute::UseLastModified` nicht eingestellt ist.

Bei Bild- und SVG-Inhalten wird `catalog::TimeStamp` auch für die Katalogbasierte Cache-Überprüfung verwendet (siehe ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Eigenschaften {#section-2298a384b5cb43929542655c5a49beb2}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* liegt zwischen 0 und 23.

*`zzz`* ist ein 3- oder 4-stelliger Zeitzonencode wie GMT oder PST. Berücksichtigen Sie die Sommerzeit im Zeitzonencode. Beispiel: PST für Pacific Standard Time (PST) und PDT (Pacific Daylight Savings Time).

*`offset`* ist ein Zeitzonenversatz in Stunden oder  `hours:minutes`, relativ zum GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente der String-formatierten Datums-/Uhrzeitwerte müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei ` *`catalog`*.ini` verwendet.

## Standard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` wenn das Feld leer ist oder nicht vorhanden ist.

## Verwandte Themen {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
