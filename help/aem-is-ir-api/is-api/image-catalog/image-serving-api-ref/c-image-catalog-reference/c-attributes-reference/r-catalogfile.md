---
description: Pfade für Bilddatendateien. Gibt die Dateien an, die die Bilddaten für diesen Katalog enthalten.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---


# CatalogFile{#catalogfile}

Pfade für Bilddatendateien. Gibt die Dateien an, die die Bilddaten für diesen Katalog enthalten.

Bilddatendateien werden in der angegebenen Reihenfolge geladen. Wenn derselbe `catalog::Id`-Wert in mehr als einem Datensatz auftritt (entweder in derselben oder in unterschiedlichen Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-6da55f145ecd4e31a5de52637a436983}

Ein oder mehrere durch Kommas getrennte Textzeichenfolgenwerte. Optional. Jeder Wert muss ein absoluter Dateipfad oder Pfad relativ zum Katalogordner sein.

## Standard {#section-80f91cd7a6b2479ebb310319e9c74da7}

Leer, was bedeutet, dass dieser Bildkatalog keine Bilddaten enthält.

## Verwandte Themen {#section-910b67c5041d44d99a105ad43ff63a37}

[Katalogdatenfelder](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
