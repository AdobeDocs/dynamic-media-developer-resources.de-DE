---
description: PostScript-Dateioptionen.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 13%

---

# PostScriptOptions{#postscriptoptions}

PostScript-Dateioptionen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| verarbeiten | `xsd:string` | Auswahl des PostScript-Prozesses. |
| Auflösung | `xsd:double` | Dateiauflösung. |
| Farbraum | `xsd:string` | PostScript-Farbraummodus. |
| alpha | `xsd:boolean` | Ob die Datei in ein Bild gerastert werden soll. Wenn dies der Fall ist, wird ein transparenter Hintergrund erstellt, wenn die Originaldatei auf diese Weise definiert ist. Wird im Allgemeinen verwendet, um überlagernde Logos zu erstellen. |
| extractSearchWords | `xsd:boolean` | Ob Suchbegriffe aus der PostScript-Datei extrahiert werden sollen. |
