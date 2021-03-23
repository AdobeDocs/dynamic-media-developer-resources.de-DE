---
description: Dateipfad für Schriftmetriken. Pfad und Name einer Schriftartmetrikdatei, einschließlich Dateisuffix.
seo-description: Dateipfad für Schriftmetriken. Pfad und Name einer Schriftartmetrikdatei, einschließlich Dateisuffix.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# MetricsPath{#metricspath}

Dateipfad für Schriftmetriken. Pfad und Name einer Schriftartmetrikdatei, einschließlich Dateisuffix.

Wird für Adobe Type 1-Schriftarten verwendet. Wenn keine Angabe gemacht wird, versucht der Server, eine Schriftartmetrikdatei im selben Ordner zu finden, in dem sich die Hauptschriftartdatei befindet. Es tritt ein Fehler auf, wenn eine erforderliche Schriftartmetrikdatei zum Rendern nicht gefunden werden kann.

## Eigenschaften {#section-955268c581574875b05253d9e14544f3}

Textzeichenfolge. Optional für Adobe Type 1-Dateien. Muss leer oder ein gültiger Image-Server-Dateipfad sein, entweder absolut oder relativ zu `attribute::RootPath`.

## Standard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Keine.

## Verwandte Themen {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
