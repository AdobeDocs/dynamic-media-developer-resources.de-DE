---
description: Pfad
solution: Experience Manager
title: Pfad
topic: Scene7 Image Serving - Image Rendering API
uuid: d1ed8a98-60eb-4bdb-884e-ea08c018d834
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 6%

---


# Pfad{#path}

Der Server verwendet die unter [Verwalten der Quelldaten](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) beschriebenen Pfadauflösungsregeln, um die Datendatei zu finden.

## Eigenschaften {#section-72d9edc532ad43349afcb4df22e1c692}

Textzeichenfolge. Erforderlich für Bild- und SVG-Datensätze, kann für Vorlagendatensätze leer sein. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Image Server-Dateipfad handeln. attribute::DefaultExt wird angehängt, wenn kein Dateisuffix vorhanden ist.

## Unterstützte Bilddateiformate {#section-8d6443c883aa48aaa00316fe9661aaa8}

Eine vollständige Liste der unterstützten Bilddateiformate finden Sie in der Beschreibung des Bildkonverters (IC).

Anwendungen, bei denen Bilddaten in verschiedenen Auflösungen benötigt werden, funktionieren am besten, wenn das Scene7 Pyramid TIFF (PTIFF)-Format mit mehreren Auflösungen verwendet wird. Das IC-Dienstprogramm wird zum Erstellen von PTIFF-Bildern aus jedem unterstützten Bildformat verwendet.

## Standard {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Keine.

## Verwandte Themen {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC-Dienstprogramm](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [Attribut::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [Attribut::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
