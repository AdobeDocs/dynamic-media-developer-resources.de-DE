---
description: Suffix der Standardbilddatei. An den Feldwert "Katalogpfad"(oder "Katalogmaskepfad") angehängt, wenn der Pfad kein Dateisuffix enthält
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# DefaultExt{#defaultext}

Suffix der Standardbilddatei. Dem Feldwert catalog::Path (oder catalog::MaskPath) angehängt, wenn der Pfad kein Dateisuffix enthält

Ein Dateisuffix besteht aus einem Punkt und einem oder mehreren Zeichen zwischen dem Punkt und dem Ende der Zeichenfolge. Das Suffix wird an den HTTP-Pfad angehängt, wenn der Pfad nicht zu einem Katalogeintrag aufgelöst wird und das letzte Pfadelement kein Dateisuffix enthält.

## Eigenschaften {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Textzeichenfolge. Muss ein vorangestelltes &#39;&#39; enthalten. und ein oder mehrere Zeichen.

## Standard {#section-1194c36ffe0748c5b9ff7d732a506588}

Vererbt von `default::DefaultExt`, wenn nicht definiert. Wenn definiert, aber leer, wird bei der Verwendung dieses Katalogs kein Standardsuffix auf Bildnamen angewendet.

## Verwandte Themen {#section-d7c408b979844643adff8258f500eb7c}

[Katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
