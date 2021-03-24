---
description: Katalogdatensatzkennung
solution: Experience Manager
title: Id
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

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