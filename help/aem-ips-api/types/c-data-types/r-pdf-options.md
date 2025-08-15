---
description: PDF-Dateioptionen.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF-Dateioptionen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| verarbeiten | `xsd:string` | Auswahl von &quot;PDF-Prozessen“. |
| Auflösung | `xsd:double` | Dateiauflösung. |
| Farbraum | `xsd:string` | Auswahl des Post-Script-Farbraummodus. |
| pdfCatalog | `xsd:boolean` | Gibt an, ob ein mehrseitiger PDF nach dem Rendern in einem E-Katalog kombiniert werden soll (Standard ist „true„). |
| extractSearchWords | `xsd:boolean` | Ob Suchbegriffe aus der PDF-Datei extrahiert werden sollen. |
| extractLinks | `xsd:boolean` | Gibt an, ob PDF-Links in Imagemaps extrahiert werden sollen, die den gerasterten Seiten in IPS zugewiesen wurden. |
