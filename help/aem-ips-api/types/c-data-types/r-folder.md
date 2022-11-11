---
description: Hierarchische Datei oder Asset-Speicherobjekt. Ordner können einen (oder mehrere) Unterordner enthalten.
solution: Experience Manager
title: Ordner
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 8%

---

# [!DNL Folder]{#folder}

Hierarchische Datei oder Asset-Speicherobjekt. Ordner können einen (oder mehrere) Unterordner enthalten.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| folderHandle | `xsd:string` | Ordner-Handle. |
| [!DNL path] | `xsd:string` | Ordnerpfad. |
| lastModified | `xsd:dateTime` | Datum der letzten Änderung. |
| childLastModified | `xsd:dateTime` | Datum der letzten Änderung für Unterordner und untergeordnete Ordner-Assets. |
| permissionsSetHandle | `xsd:string` | Umgang mit Ordnerberechtigungen |
| hasSubfolder | `types:Boolean` | Bestimmt, ob ein Ordner Unterordner enthält. |
| subfolderArray | `types:FolderArray` | Ein Array von Unterordnern in einem Ordner. |
