---
description: Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Abziehbilddatei.
solution: Experience Manager
title: Pfad *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Pfad *{#path}

Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Abziehbilddatei.

Der Server kombiniert diesen Wert mit `attribute::RootPath`, um den tatsächlichen Bilddateipfad zu erstellen. Kann auch ein absoluter Pfad sein.

Wird verwendet, um die Texturbilddatei für Textur-, Schrank- und Fensterabdeckungsmaterialien und die RGB- oder RGBA-Bilddatei für Abziehbild- und Wandbegrenzungsmaterialien anzugeben. Nicht alle Schrank- und Fensterabdeckmaterialien erfordern ein separates wiederholbares Texturbild.

## Eigenschaften {#section-8c12ea24f21d4472be677581893e6681}

Text-String Erforderlich für Textur- und Abziehmaterialien, optional für Schrank- und Fensterabdeckmaterialien. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Dateipfad handeln. Muss für einfarbige Materialien leer sein.

## Unterstützte Dateiformate {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Das Bild-Rendering unterstützt dieselben Quellbildformate wie Dynamic Media Image Serving.

Anwendungen, für die Bilddaten in mehreren Auflösungen erforderlich sind, bieten die beste Leistung bei Verwendung des PTIFF-Formats (Dynamic Media Pyramid TIFF) mit mehreren Auflösungen. Image Serving beinhaltet das Image Converter-Dienstprogramm (IC), das PTIFF-Bilder aus jedem unterstützten Format erstellt.

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des IC-Dienstprogramms in der Dokumentation zu Image-Serving .

## Standard {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Keine.

## Verwandte Themen {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC-Dienstprogramm](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
