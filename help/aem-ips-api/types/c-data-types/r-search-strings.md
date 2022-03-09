---
description: Aus einer PDF-Datei extrahierter Suchzeichenfolgen-Datensatz.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 12%

---

# SearchStrings{#searchstrings}

Aus einer PDF-Datei extrahierter Suchzeichenfolgen-Datensatz.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| searchString | `xsd:string` | Suchzeichenfolgentext. |
| keywordsArray | `types:KeywordsArray` | Array von Suchbegriffen in der Suchzeichenfolge. |
| status | `xsd:boolean` | True , wenn die Suchzeichenfolge gültig und aktiviert ist. |
| x | `xsd:int` | X Achsenposition der Suchzeichenfolge. |
| y | `xsd:int` | Y-Achsenposition der Suchzeichenfolge. |
| Breite | `xsd:int` | Breite der Suchzeichenfolge. |
| Höhe | `xsd:int` | Höhe der Suchzeichenfolge. |
| fontName | `xsd:string` | Name der in der Suchzeichenfolge verwendeten Schriftart. |
| pointSize | `xsd:string` | Schriftgröße. |
