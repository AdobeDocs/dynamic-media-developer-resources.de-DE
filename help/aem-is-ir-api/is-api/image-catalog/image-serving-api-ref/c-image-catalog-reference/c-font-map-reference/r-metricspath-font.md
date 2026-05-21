---
description: Dateipfad für Schriftmetriken. Pfad und Name einer Schriftmetrikdatei, einschließlich Dateisuffix.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
TQID: 'https://experienceleague.adobe.com/XPXcnrT94IfPupctNoxqN7-qYCuxdeoqXQeBkM1Un4k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 3%

---

# MetricsPath{#metricspath}

Dateipfad für Schriftmetriken. Pfad und Name einer Schriftmetrikdatei, einschließlich Dateisuffix.

Wird für Adobe Type 1-Schriftarten verwendet. Wenn nicht anders angegeben, versucht der Server, eine Schriftmetrikdatei im selben Ordner zu finden, in dem sich die Prinzipalschriftdatei befindet. Ein Fehler tritt auf, wenn eine erforderliche Schriftmetrikdatei zum Zeitpunkt des Renderns nicht gefunden werden kann.

## Eigenschaften {#section-955268c581574875b05253d9e14544f3}

Text-String Optional für Adobe Type 1-Dateien. Muss leer oder ein gültiger Bildserver-Dateipfad sein, entweder absolut oder relativ zu `attribute::RootPath`.

## Standard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Keine.

## Verwandte Themen {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
