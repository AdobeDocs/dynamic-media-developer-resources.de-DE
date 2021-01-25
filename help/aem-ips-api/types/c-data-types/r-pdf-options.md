---
description: PDF-Dateioptionen.
seo-description: PDF-Dateioptionen.
seo-title: PDFOptions
solution: Experience Manager
title: PDFOptions
topic: Dynamic Media Image Production System API
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 9%

---


# PDFOptions{#pdfoptions}

PDF-Dateioptionen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`verarbeiten`*` | `xsd:string` | Auswahl von &quot;PDF-Prozessen&quot;. |
| `*`resolution`*` | `xsd:double` | Dateiauflösung. |
| `*`Farbraum`*` | `xsd:string` | Auswahl des Colorspace-Modus nach dem Skript. |
| `*`pdfCatalog`*` | `xsd:boolean` | Ob eine mehrseitige PDF nach dem Rendern in einen E-Katalog kombiniert werden soll (Standard ist true). |
| `*`extractSearchWords`*` | `xsd:boolean` | Gibt an, ob Suchbegriffe aus der PDF-Datei extrahiert werden sollen. |
| `*`extractLinks`*` | `xsd:boolean` | Ob PDF-Links in Imagemaps extrahiert werden sollen, die den gerasterten Seiten in IPS zugewiesen sind. |

