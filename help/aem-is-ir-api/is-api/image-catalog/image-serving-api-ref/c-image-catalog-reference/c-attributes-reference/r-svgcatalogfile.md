---
description: SVG-Datendateipfade. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
TQID: 'https://experienceleague.adobe.com/m1-nKj-KiVQlN70GYy1AFAAQN-M1wnxTGmmj-e3t9AY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 3%

---

# SvgCatalogFile{#svgcatalogfile}

SVG-Datendateipfade. Gibt die Dateien an, die die SVG-Daten für diesen Katalog enthalten.

SVG-Datendateien werden nach allen Bilddatendateien in der exakt angegebenen Reihenfolge geladen. Wenn derselbe `catalog::Id` in mehr als einem Datensatz auftritt (entweder im selben oder in anderen Bilddateien oder SVG-Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-fc2d549f76474792837b2b92ec2087ea}

Ein oder mehrere durch Kommas getrennte Textzeichenfolgenwerte. Optional. Jeder Wert muss ein absoluter Dateipfad oder ein absoluter Pfad relativ zum Katalogordner sein.

## Standard {#section-a4e58951f3c249599665b823566433c9}

Leer, was anzeigt, dass dieser Bildkatalog keine SVG-Daten enthält.

## Verwandte Themen {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Catalog Data](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
