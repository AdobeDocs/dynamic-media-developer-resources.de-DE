---
description: Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Decal-Bilddatei.
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

Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Decal-Bilddatei.

Der Server kombiniert diesen Wert mit `attribute::RootPath` , um den Pfad der Bilddatei zu erstellen. Kann auch ein absoluter Pfad sein.

Wird verwendet, um die Texturbilddatei für Textur-, Schrank- und Fensterabdeckungsmaterialien sowie die RGB- oder RGBA-Bilddatei für Dekal- und Wandbegrenzungsmaterialien anzugeben. Nicht alle Schrank- und Fensterabdeckungsmaterialien erfordern ein separates wiederholbares Texturbild.

## Eigenschaften {#section-8c12ea24f21d4472be677581893e6681}

Textzeichenfolge. Erforderlich für Textur- und Dekormaterialien, optional für Schrank- und Fensterbedeckungsmaterialien. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Dateipfad handeln. Muss für feste Farbstoffe leer sein.

## Unterstützte Dateiformate {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Das Bild-Rendering unterstützt dieselben Quellbildformate wie das Dynamic Media-Bildserving.

Anwendungen, die Bilddaten in mehreren Auflösungen erfordern, eignen sich am besten für die Verwendung des PTIFF-Multiauflösungsformats (Dynamic Media Pyramid TIFF). Image Serving umfasst das Dienstprogramm Image Converter (IC) , mit dem PTIFF-Bilder aus einem beliebigen unterstützten Format erstellt werden.

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Dokumentation zu Image Serving in der Beschreibung des IC-Dienstprogramms .

## Standard {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Keine.

## Verwandte Themen {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
