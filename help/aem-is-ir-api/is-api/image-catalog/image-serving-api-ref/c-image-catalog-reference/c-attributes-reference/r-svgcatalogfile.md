---
description: SVG von Datendateipfaden. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# SvgCatalogFile{#svgcatalogfile}

SVG von Datendateipfaden. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.

SVG-Datendateien werden nach allen Bilddatendateien in der angegebenen exakten Reihenfolge geladen. Wenn derselbe `catalog::Id` in mehr als einem Datensatz auftritt (entweder im selben oder in anderen Bild- oder SVG-Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-fc2d549f76474792837b2b92ec2087ea}

Ein oder mehrere durch Kommas getrennte Textzeichenfolgenwerte. Optional. Jeder Wert muss ein absoluter Dateipfad oder ein absoluter Pfad relativ zum Katalogordner sein.

## Standard {#section-a4e58951f3c249599665b823566433c9}

Leer, was anzeigt, dass dieser Bildkatalog keine SVG-Daten enthält.

## Verwandte Themen {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Catalog Data](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
