---
description: Pfad der Bilddatei.
solution: Experience Manager
title: Pfad
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
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