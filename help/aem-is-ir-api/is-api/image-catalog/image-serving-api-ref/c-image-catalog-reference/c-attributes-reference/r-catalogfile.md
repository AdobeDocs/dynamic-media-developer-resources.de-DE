---
description: Bilddatendateipfade. Gibt die Dateien an, die die Bilddaten für diesen Katalog enthalten.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# CatalogFile{#catalogfile}

Bilddatendateipfade. Gibt die Dateien an, die die Bilddaten für diesen Katalog enthalten.

Bilddatendateien werden in der angegebenen Reihenfolge geladen. Wenn derselbe `catalog::Id` -Wert in mehr als einem Datensatz auftritt (entweder in derselben oder in unterschiedlichen Katalogdateien), hat die letzte Instanz Vorrang.

## Eigenschaften {#section-6da55f145ecd4e31a5de52637a436983}

Ein oder mehrere Textzeichenwerte, durch Kommas getrennt. Optional. Jeder Wert muss ein absoluter Dateipfad oder Pfad relativ zum Katalogordner sein.

## Standard {#section-80f91cd7a6b2479ebb310319e9c74da7}

Leer, was bedeutet, dass dieser Bildkatalog keine Bilddaten enthält.

## Verwandte Themen {#section-910b67c5041d44d99a105ad43ff63a37}

[Katalogdatenfelder](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
