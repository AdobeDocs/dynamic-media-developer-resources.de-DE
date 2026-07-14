---
description: PDF-Dateioptionen.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 68
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

