---
description: Standardsuffix der Bilddatei. An den Feldwert "Katalogpfad"(oder "Katalogmaskepfad") angehängt, wenn der Pfad kein Dateisuffix enthält
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# DefaultExt{#defaultext}

Standardsuffix der Bilddatei. An den Feldwert catalog::Path (oder catalog::MaskPath) angehängt, wenn der Pfad kein Dateisuffix enthält

Ein Dateisuffix besteht aus einem Punkt und einem oder mehreren Zeichen zwischen dem Punkt und dem Ende der Zeichenfolge. Das Suffix wird an den HTTP-Pfad angehängt, wenn der Pfad nicht zu einem Katalogeintrag aufgelöst wird und das letzte Pfadelement kein Dateisuffix enthält.

## Eigenschaften {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Textzeichenfolge. Muss ein führendes &#39;.&#39; enthalten und ein oder mehrere Zeichen.

## Standard {#section-1194c36ffe0748c5b9ff7d732a506588}

Wird von `default::DefaultExt` übernommen, falls nicht definiert. Wenn definiert, aber leer, wird bei Verwendung dieses Katalogs kein Standardsuffix auf Bildnamen angewendet.

## Verwandte Themen {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
