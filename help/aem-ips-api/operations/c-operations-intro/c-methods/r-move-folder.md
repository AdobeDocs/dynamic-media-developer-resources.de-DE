---
description: Verschieben Sie einen Ordner an einen neuen Speicherort.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '60'
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
| companyHandle | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| folderHandle | `xsd:string` | Ja | Ordner-Handle. |
| destFolderHandle | `xsd:string` | Ja | Verarbeiten Sie den Zielordner. |

**Output (moveFolderReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| folderHandle | `xsd:string` | Ja | Verarbeiten Sie den verschobenen Ordner. |

## Beispiele {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Anfrage**

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
