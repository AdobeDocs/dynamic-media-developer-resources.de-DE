---
description: Pfad der Bilddatei.
solution: Experience Manager
title: Pfad
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Pfad{#path}

Pfad der Bilddatei.

Relativer oder absoluter Pfad und Name der Quellbilddatei, die mit diesem Katalogdatensatz verknüpft ist. Der Server verwendet die unter Verwalten der Quelldaten beschriebenen Pfadauflösungsregeln, um die Datendatei zu finden.

## Eigenschaften {#path-properties}

Textzeichenfolge. Für Bilddatensätze erforderlich, kann für Vorlagendatensätze leer sein. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Image Server-Dateipfad handeln. attribute::DefaultExt wird angehängt, wenn kein Dateisuffix vorhanden ist.

## Unterstützte Bilddateiformate {#path-supported-image-file-formats}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des Hilfsprogramms Image Converter (IC).

Anwendungen, die Bilddaten in verschiedenen Auflösungen erfordern, sind am besten geeignet, wenn Sie das Dynamic Media Pyramid TIFF (PTIFF)-Format mit mehreren Auflösungen verwenden. Das IC-Dienstprogramm wird zum Erstellen von PTIFF-Bildern aus jedem unterstützten Bildformat verwendet.

## Standard {#path-default}

Keine.

## Verwandte Themen {#path-seealso}

[IC-Dienstprogramm](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [Attribut::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [Attribut::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->