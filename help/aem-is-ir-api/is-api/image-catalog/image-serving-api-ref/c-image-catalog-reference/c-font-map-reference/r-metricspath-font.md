---
description: Dateipfad für Schriftmetriken. Pfad und Name einer Schriftartmetrikdatei, einschließlich Dateisuffix.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# MetricsPath{#metricspath}

Dateipfad für Schriftmetriken. Pfad und Name einer Schriftartmetrikdatei, einschließlich Dateisuffix.

Wird für Adobe Type 1-Schriftarten verwendet. Wenn nichts angegeben ist, versucht der Server, eine Schriftartmetrikdatei im selben Ordner zu finden, in dem sich die Hauptschriftartdatei befindet. Wenn eine erforderliche Schriftartmetrikdatei zum Rendern nicht gefunden werden kann, tritt ein Fehler auf.

## Eigenschaften {#section-955268c581574875b05253d9e14544f3}

Textzeichenfolge. Optional für Adobe Type 1-Dateien. Muss leer oder ein gültiger Dateipfad für den Image-Server sein, entweder absolut oder relativ zu `attribute::RootPath`.

## Standard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Keine.

## Verwandte Themen {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
