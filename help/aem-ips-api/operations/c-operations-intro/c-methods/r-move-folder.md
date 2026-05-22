---
description: Verschiebt einen Ordner an einen neuen Speicherort.
solution: Experience Manager
title: MoveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
TQID: 'https://experienceleague.adobe.com/xnBMdEtQN9m8JZZNfa8mPR1Zl6XyS-zYwM5JJzPREv0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 25%

---

# MoveFolder{#movefolder}

Verschiebt einen Ordner an einen neuen Speicherort.

Syntax

## Autorisierte Benutzertypen {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Eingabe (moveFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| folderHandle | `xsd:string` | Ja | Ordner-Handle |
| destFolderHandle | `xsd:string` | Ja | Verarbeiten Sie den Zielordner. |

**Ausgabe (moveFolderReturn)**

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
