---
description: Statischer Stammpfad für Inhaltsdaten. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für die statischen Inhaltsdaten dieses Bildkatalogs.
solution: Experience Manager
title: StaticContentRootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---

# StaticContentRootPath{#staticcontentrootpath}

Statischer Stammpfad für Inhaltsdaten. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für die statischen Inhaltsdaten dieses Bildkatalogs.

Weitere Informationen zu Serverstammpfaden finden Sie unter [Verwalten von Source-Daten](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) .

## Eigenschaften {#section-f8e3986096294b36948d43aafdc3e795}

Textzeichenfolge. Muss leer, ein gültiges relatives Dateipfadsegment oder ein absoluter Pfad sein. Sollte keine Trennzeichen für vorangehende und nachfolgende Pfadelemente enthalten.

## Standard {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

Wird von `default::StaticContentsRootPath` übernommen, falls nicht definiert. Wenn definiert, aber leer, trägt es nicht zum Stammverzeichnis der Quelldatei bei.

## Verwandte Themen {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) , [Verwalten von Source-Daten](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
