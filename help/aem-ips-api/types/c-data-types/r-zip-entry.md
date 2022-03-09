---
description: Ein Eintrag in einer ZIP-Datei.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 13%

---

# ZipEntry{#zipentry}

Ein Eintrag in einer ZIP-Datei.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| name | `xsd:string` | Name der Einsendung. |
| isDirectory | `xsd:boolean` | Bestimmt, ob der Eintrag ein Verzeichnis ist. |
| lastModified | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung. |
| compressionSize | `xsd:long` | Komprimierte Größe. |
| uncompressionSize | `xsd:long` | Unkomprimierte Größe. |
