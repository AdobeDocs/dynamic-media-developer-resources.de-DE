---
description: Zeitstempel
solution: Experience Manager
title: Zeitstempel
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
TQID: 'https://experienceleague.adobe.com/n-LXS-OEhuBOkse44eQ0HTHV-Bx5BRH3AjgE0xInqK8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 200
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
