---
description: Hierarchische Datenspeicherung oder Asset-Objekt. Ordner können einen (oder mehrere) Unterordner enthalten.
solution: Experience Manager
title: Ordner
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# Ordner{#folder}

Hierarchische Datenspeicherung oder Asset-Objekt. Ordner können einen (oder mehrere) Unterordner enthalten.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Ordner-Handle. |
| `*`Pfade`*` | `xsd:string` | Ordnerpfad. |
| `*`lastModified`*` | `xsd:dateTime` | Datum der letzten Änderung. |
| `*`childLastModified`*` | `xsd:dateTime` | Datum der letzten Änderung für untergeordnete Unterordner und Ordner-Assets. |
| `*`permissionsSetHandle`*` | `xsd:string` | Ordnerberechtigungshandle. |
| `*`hasSubfolder`*` | `types:Boolean` | Bestimmt, ob ein Ordner Unterordner enthält. |
| `*`subfolderArray`*` | `types:FolderArray` | Ein Array von Unterordnern in einem Ordner. |

