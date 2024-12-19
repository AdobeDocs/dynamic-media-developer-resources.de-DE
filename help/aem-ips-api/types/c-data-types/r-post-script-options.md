---
description: PostScript-Dateioptionen.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
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
