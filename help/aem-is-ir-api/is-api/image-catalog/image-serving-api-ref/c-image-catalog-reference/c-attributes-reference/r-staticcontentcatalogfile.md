---
description: Datendateipfade für statischen Inhalt. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Datendateipfade für statischen Inhalt. Gibt die Dateien an, die die statischen Inhaltsdaten für diesen Katalog enthalten.

Datendateien für statische Inhalte werden in der angegebenen Reihenfolge geladen. Wenn derselbe `static::Id`-Wert in mehr als einem Datensatz auftritt (entweder in derselben oder in unterschiedlichen Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Ein oder mehrere durch Kommas getrennte Textzeichenfolgenwerte. Optional. Jeder Wert muss ein absoluter Dateipfad oder Pfad relativ zum Katalogordner sein.

## Standard {#section-702edfbc00c54fc29e412a3ff99fef2b}

Leer, was bedeutet, dass dieser Bildkatalog keine statischen Inhaltsdaten enthält.

## Verwandte Themen {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Katalogdaten](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
