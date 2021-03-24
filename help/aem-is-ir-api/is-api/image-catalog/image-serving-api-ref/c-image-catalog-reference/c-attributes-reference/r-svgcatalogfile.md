---
description: SVG-Datendateipfade. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# SvgCatalogFile{#svgcatalogfile}

SVG-Datendateipfade. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.

SVG-Datendateien werden nach allen Bilddatendateien in der angegebenen Reihenfolge geladen. Wenn derselbe `catalog::Id`-Wert in mehr als einem Datensatz auftritt (entweder in derselben oder in einer anderen Bild- oder SVG-Katalogdatei), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-fc2d549f76474792837b2b92ec2087ea}

Ein oder mehrere durch Kommas getrennte Textzeichenfolgenwerte. Optional. Jeder Wert muss ein absoluter Dateipfad oder Pfad relativ zum Katalogordner sein.

## Standard {#section-a4e58951f3c249599665b823566433c9}

Leer, was bedeutet, dass dieser Bildkatalog keine SVG-Daten enthält.

## Verwandte Themen {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Katalogdaten](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29),  [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
