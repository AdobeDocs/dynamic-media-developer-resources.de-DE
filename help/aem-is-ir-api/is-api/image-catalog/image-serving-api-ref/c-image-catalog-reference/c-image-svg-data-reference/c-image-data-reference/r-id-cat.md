---
description: Katalogdatensatzkennung
solution: Experience Manager
title: Id
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 8%

---


# Id {#id}

Indexschlüsselwert, mit dem Datensätze in der Bilddatendatei vom Plattformserver nachgeschlagen werden.

In der Regel eine kurze und eindeutige Bildkennung, z. B. eine SKU-Nummer, möglicherweise mit einer Art Bildsuffix, wenn eine SKU mehrere Bilder hat. Kann auch eine komplexere Zeichenfolge sein, die eher wie ein Dateipfad aussieht, um eine einfache Retropassung von Websites mit Image Serving zu unterstützen.

## Eigenschaften {#id-properties}

Textzeichenfolge. Erforderlich. Primär-Indexschlüssel für die Bilddatentabelle. Jeder Katalog::Id-Wert muss innerhalb der Tabelle eindeutig sein.

## Standard {#id-default}

Keine.

## Verwandte Themen {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)