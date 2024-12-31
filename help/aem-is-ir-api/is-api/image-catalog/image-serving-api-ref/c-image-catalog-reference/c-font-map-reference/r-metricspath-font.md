---
description: Dateipfad für Schriftmetriken. Pfad und Name einer Schriftmetrikdatei, einschließlich Dateisuffix.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# MetricsPath{#metricspath}

Dateipfad für Schriftmetriken. Pfad und Name einer Schriftmetrikdatei, einschließlich Dateisuffix.

Wird für Schriftarten der Adobe Type 1 verwendet. Wenn nicht anders angegeben, versucht der Server, eine Schriftmetrikdatei im selben Ordner zu finden, in dem sich die Prinzipalschriftdatei befindet. Ein Fehler tritt auf, wenn eine erforderliche Schriftmetrikdatei zum Zeitpunkt des Renderns nicht gefunden werden kann.

## Eigenschaften {#section-955268c581574875b05253d9e14544f3}

Text-String Optional für Dateien der Adobe Type 1. Muss leer oder ein gültiger Bildserver-Dateipfad sein, entweder absolut oder relativ zu `attribute::RootPath`.

## Standard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Keine.

## Verwandte Themen {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
