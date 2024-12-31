---
description: Ein Eintrag in einer ZIP-Datei.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 14%

---

# [!DNL ZipEntry]{#zipentry}

Ein Eintrag in einer ZIP-Datei.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| name | `xsd:string` | Name des Eintrags. |
| isDirectory | `xsd:boolean` | Bestimmt, ob der Eintrag ein Verzeichnis ist. |
| lastModify | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung. |
| compressionSize | `xsd:long` | Komprimierte Größe. |
| unkomprimiertGröße | `xsd:long` | Unkomprimierte Größe. |
