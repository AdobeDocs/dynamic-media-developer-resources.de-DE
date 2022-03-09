---
description: PDF-Dateioptionen.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 11%

---

# PDFOptions{#pdfoptions}

PDF-Dateioptionen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| verarbeiten | `xsd:string` | Auswahl von &quot;PDF-Prozessen&quot;. |
| Auflösung | `xsd:double` | Dateiauflösung. |
| Farbraum | `xsd:string` | Auswahl des Farbmodus nach dem Skript. |
| pdfCatalog | `xsd:boolean` | Ob nach dem Rendern eine mehrseitige PDF in einen E-Katalog kombiniert werden soll (Standard ist &quot;true&quot;). |
| extractSearchWords | `xsd:boolean` | Ob Suchbegriffe aus der PDF-Datei extrahiert werden sollen. |
| extractLinks | `xsd:boolean` | Ob PDF-Links in Imagemaps extrahiert werden sollen, die den gerasterten Seiten innerhalb von IPS zugewiesen sind. |
