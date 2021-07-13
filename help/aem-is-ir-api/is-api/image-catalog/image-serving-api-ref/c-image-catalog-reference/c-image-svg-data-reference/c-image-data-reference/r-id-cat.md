---
description: Katalogdatensatzkennung
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# ID {#id}

Indexschlüsselwert, anhand dessen Datensätze in der Bilddatendatei vom Platform-Server nachgeschlagen werden.

In der Regel eine kurze und eindeutige Bild-ID, z. B. eine SKU-Nummer, möglicherweise mit einer Art Bildsuffix, wenn eine SKU mehrere Bilder hat. Kann auch eine komplexere Zeichenfolge sein, die eher wie ein Dateipfad aussieht, um eine einfache Rückverfolgung von Websites mit Image Serving zu unterstützen.

## Eigenschaften {#id-properties}

Textzeichenfolge. Erforderlich. Primärer Indexschlüssel für die Bilddatentabelle. Jeder catalog::Id -Wert muss innerhalb der Tabelle eindeutig sein.

## Standard {#id-default}

Keine.

## Verwandte Themen {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
