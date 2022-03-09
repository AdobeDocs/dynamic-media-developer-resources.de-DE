---
description: Hierarchische Datei oder Asset-Speicherobjekt. Ordner können einen (oder mehrere) Unterordner enthalten.
solution: Experience Manager
title: Ordner
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# Ordner{#folder}

Hierarchische Datei oder Asset-Speicherobjekt. Ordner können einen (oder mehrere) Unterordner enthalten.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| folderHandle | `xsd:string` | Ordner-Handle. |
| Pfade | `xsd:string` | Ordnerpfad. |
| lastModified | `xsd:dateTime` | Datum der letzten Änderung. |
| childLastModified | `xsd:dateTime` | Datum der letzten Änderung für Unterordner und untergeordnete Ordner-Assets. |
| permissionsSetHandle | `xsd:string` | Umgang mit Ordnerberechtigungen |
| hasSubfolder | `types:Boolean` | Bestimmt, ob ein Ordner Unterordner enthält. |
| subfolderArray | `types:FolderArray` | Ein Array von Unterordnern in einem Ordner. |
