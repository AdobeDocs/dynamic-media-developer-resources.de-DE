---
description: Zeitstempel
solution: Experience Manager
title: Zeitstempel
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# Zeitstempel{#timestamp}

Wenn `attribute::UseLastModified` festgelegt ist, wird der `catalog::TimeStamp` in der HTTP-Antwort als HTTP-Header der letzten Änderung zurückgegeben. Der Last-Modified-Header wird für statische Inhalte immer zurückgegeben, auch wenn `attribute::UseLastModified` nicht festgelegt ist.

Für Bild- und SVG-Inhalte wird `catalog::TimeStamp` auch für die katalogbasierte Cache-Validierung verwendet (siehe [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Eigenschaften {#section-2298a384b5cb43929542655c5a49beb2}

Datum/Uhrzeit-Wert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* liegt im Bereich von 0 bis 23.

*`zzz`* ist ein drei- oder vierstelliger Zeitzonencode wie „GMT“ oder „PST“. Berücksichtigen Sie die Sommerzeit im Zeitzonen-Code. Beispiel: „PST“ für Pacific Standard Time und „PDT“ für Pacific Daylight Saving Time).

*`offset`* ist ein Zeitzonenversatz in Stunden oder `hours:minutes`, relativ zu GMT. „PDT“ entspricht beispielsweise „GMT -7“.

Alle Elemente von Datums-/Uhrzeitwerten im Zeichenfolgenformat müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der `*`Katalog`*.ini`-Datei verwendet.

## Standard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp`, ob das Feld leer oder nicht vorhanden ist.

## Verwandte Themen {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
