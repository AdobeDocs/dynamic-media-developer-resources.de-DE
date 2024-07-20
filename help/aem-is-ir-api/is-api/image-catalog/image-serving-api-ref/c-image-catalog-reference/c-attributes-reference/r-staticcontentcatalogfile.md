---
description: Datendateipfade für statische Inhaltskataloge. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

Datendateipfade für statische Inhaltskataloge. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.

Datendateien des statischen Inhaltskatalogs werden in der angegebenen Reihenfolge geladen. Wenn derselbe `static::Id` -Wert in mehr als einem Datensatz auftritt (entweder in derselben oder in unterschiedlichen Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Ein oder mehrere Textzeichenwerte, durch Kommas getrennt. Optional. Jeder Wert muss ein absoluter Dateipfad oder Pfad relativ zum Katalogordner sein.

## Standard {#section-702edfbc00c54fc29e412a3ff99fef2b}

Leer, was bedeutet, dass dieser Bildkatalog keine statischen Inhaltsdaten enthält.

## Verwandte Themen {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Katalogdaten](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
