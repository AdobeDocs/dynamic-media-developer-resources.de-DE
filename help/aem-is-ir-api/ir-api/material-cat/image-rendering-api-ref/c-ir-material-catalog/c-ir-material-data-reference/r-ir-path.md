---
description: Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Dezimalbilddatei.
seo-description: Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Dezimalbilddatei.
seo-title: Pfad *
solution: Experience Manager
title: Pfad *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 3%

---


# Pfad *{#path}

Pfad der Bilddatei. Relativer Pfad und Name einer Textur- oder Dezimalbilddatei.

Der Server kombiniert diesen Wert mit `attribute::RootPath`, um den tatsächlichen Pfad der Bilddatei zu erstellen. Kann auch ein absoluter Pfad sein.

Dient zur Angabe der Texturbilddatei für Textur-, Schrank- und Fensterbezugsmaterialien sowie der RGB- oder RGBA-Bilddatei für Dekorationsmaterial und Wandbegrenzungsmaterialien. Nicht alle Schrank- und Fensterbedeckungsmaterialien erfordern ein separates, wiederholbares Texturbild.

## Eigenschaften {#section-8c12ea24f21d4472be677581893e6681}

Textzeichenfolge. Erforderlich für Textur- und Dekormaterialien, optional für Schrank- und Fensterbezugsmaterialien. Bei Angabe muss es sich um einen gültigen relativen oder absoluten Dateipfad handeln. Muss leer sein für feste Farbmaterialien.

## Unterstützte Dateiformate {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Das Image Rendering unterstützt dieselben Quellbildformate wie das Scene7 Image Serving.

Anwendungen, bei denen Bilddaten in verschiedenen Auflösungen benötigt werden, funktionieren am besten, wenn das Scene7 Pyramid TIFF (PTIFF)-Format mit mehreren Auflösungen verwendet wird. Image Serving enthält das Dienstprogramm Image Converter (IC), mit dem PTIFF-Bilder aus jedem unterstützten Format erstellt werden.

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Dokumentation zu Image Serving in der Beschreibung des IC-Dienstprogramms.

## Standard {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Keine.

## Verwandte Themen {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC-Dienstprogramm](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [Attribut::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
