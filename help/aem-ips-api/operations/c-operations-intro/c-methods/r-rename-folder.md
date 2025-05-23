---
description: Benennt einen Ordner um.
solution: Experience Manager
title: Ordner umbenennen
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# Ordner umbenennen{#renamefolder}

Benennt einen Ordner um.

Syntax

## Autorisierte Benutzertypen {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Asset haben.

## Parameter {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Eingabe (renameFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Verarbeiten Sie das Unternehmen mit Ordnern, die Sie umbenennen möchten. |
| folderHandle | `xsd:string` | Ja | Verarbeiten Sie den Ordner. |
| folderName | `xsd:string` | Ja | Neuer Ordnername. |

**Ausgabe (renameFolderReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| folderHandle | `xsd:string` | Ja | Verarbeiten Sie den umbenannten Ordner. |

## Beispiele {#section-98bdd2f88d164f488676e90aba1dc864}

Dieses Codebeispiel benennt einen Ordner um.

**Anfrage**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Antwort**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
