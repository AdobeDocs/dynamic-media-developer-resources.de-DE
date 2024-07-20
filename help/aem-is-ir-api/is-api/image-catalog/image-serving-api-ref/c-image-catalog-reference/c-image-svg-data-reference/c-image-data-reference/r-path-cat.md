---
description: Pfad der Bilddatei.
solution: Experience Manager
title: Pfad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# Pfad{#path}

Pfad der Bilddatei.

Relativer oder absoluter Pfad und Name der mit diesem Katalogdatensatz verknüpften Quellbilddatei. Der Server verwendet die unter Verwalten von Source-Daten beschriebenen Regeln zur Pfadauflösung, um die Datendatei zu finden.

## Eigenschaften {#path-properties}

Textzeichenfolge. Für Bilddatensätze erforderlich, kann für Vorlagendatensätze leer sein. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Image Server-Dateipfad handeln. attribute::DefaultExt wird angehängt, wenn kein Dateisuffix vorhanden ist.

## Unterstützte Bilddateiformate {#path-supported-image-file-formats}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des Image Converter-Dienstprogramms (IC) .

Anwendungen, die Bilddaten in mehreren Auflösungen erfordern, eignen sich am besten für die Verwendung des PTIFF-Multiauflösungsformats (Dynamic Media Pyramid TIFF). Das IC-Dienstprogramm wird verwendet, um PTIFF-Bilder aus einem beliebigen unterstützten Bildformat zu erstellen.

## Standard {#path-default}

Keine.

## Verwandte Themen {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
