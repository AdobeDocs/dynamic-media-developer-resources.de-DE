---
description: SVG-Datendateipfade. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.
seo-description: SVG-Datendateipfade. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

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
