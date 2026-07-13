---
description: PostScript-Dateioptionen.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: 'https://experienceleague.adobe.com/XsIiYor0c-7I34OYazNaSF0Hx3sbZmzpTzAT1u73xxo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript-Dateioptionen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| verarbeiten | `xsd:string` | PostScript-Prozessauswahl. |
| Auflösung | `xsd:double` | Dateiauflösung. |
| Farbraum | `xsd:string` | PostScript-Farbraummodus. |
| alpha | `xsd:boolean` | Gibt an, ob die Datei in einem Bild gerastert werden soll. Wenn ja, wird ein transparenter Hintergrund erstellt, wenn die Originaldatei auf diese Weise definiert ist. Wird im Allgemeinen zum Erstellen von Überlagerungslogos verwendet. |
| extractSearchWords | `xsd:boolean` | Ob Suchbegriffe aus der PostScript-Datei extrahiert werden sollen. |

