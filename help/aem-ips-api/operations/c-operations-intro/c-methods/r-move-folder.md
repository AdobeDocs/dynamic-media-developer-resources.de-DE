---
description: Verschieben Sie einen Ordner an einen neuen Speicherort.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 25%

---


# moveFolder{#movefolder}

Verschieben Sie einen Ordner an einen neuen Speicherort.

Syntax

## Autorisierte Benutzertypen {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Input (moveFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| `*`folderHandle`*` | `xsd:string` | Ja | Ordner-Handle. |
| `*`destFolderHandle`*` | `xsd:string` | Ja | Zum Zielordner gehen. |

**Output (moveFolderReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Ja | Wechseln Sie zum verschobenen Ordner. |

## Beispiele {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Anforderung**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Antwort**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

