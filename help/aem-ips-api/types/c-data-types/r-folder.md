---
description: Hierarchische Datenspeicherung oder Asset-Objekt. Ordner können einen (oder mehrere) Unterordner enthalten.
seo-description: Hierarchische Datenspeicherung oder Asset-Objekt. Ordner können einen (oder mehrere) Unterordner enthalten.
seo-title: Ordner
solution: Experience Manager
title: Ordner
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 10%

---


# Ordner{#folder}

Hierarchische Datenspeicherung oder Asset-Objekt. Ordner können einen (oder mehrere) Unterordner enthalten.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Ordner-Handle. |
| ` *`Pfade`*` | `xsd:string` | Ordnerpfad. |
| ` *`lastModified`*` | `xsd:dateTime` | Datum der letzten Änderung. |
| ` *`childLastModified`*` | `xsd:dateTime` | Datum der letzten Änderung für untergeordnete Unterordner und Ordner-Assets. |
| ` *`permissionsSetHandle`*` | `xsd:string` | Ordnerberechtigungshandle. |
| ` *`hasSubfolder`*` | `types:Boolean` | Bestimmt, ob ein Ordner Unterordner enthält. |
| ` *`subfolderArray`*` | `types:FolderArray` | Ein Array von Unterordnern in einem Ordner. |

