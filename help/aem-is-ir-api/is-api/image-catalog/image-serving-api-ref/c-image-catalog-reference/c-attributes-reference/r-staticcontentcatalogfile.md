---
description: Datendateipfade für statischen Inhalt. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.
seo-description: Datendateipfade für statischen Inhalt. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Datendateipfade für statischen Inhalt. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.

Datendateien für statische Inhalte werden in der angegebenen Reihenfolge geladen. Wenn derselbe `static::Id` Wert in mehr als einem Datensatz auftritt (entweder in derselben oder in unterschiedlichen Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Ein oder mehrere durch Kommas getrennte Textzeichenfolgenwerte. Optional. Jeder Wert muss ein absoluter Dateipfad oder Pfad relativ zum Katalogordner sein.

## Standard {#section-702edfbc00c54fc29e412a3ff99fef2b}

Leer, was bedeutet, dass dieser Bildkatalog keine statischen Inhaltsdaten enthält.

## Verwandte Themen {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Katalogdaten](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
