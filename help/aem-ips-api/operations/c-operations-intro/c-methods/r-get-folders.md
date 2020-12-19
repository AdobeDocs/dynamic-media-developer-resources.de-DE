---
description: Gibt alle Ordner und Unterordner ab dem Ordnerpfad zurück. Die getFolders-Antwort gibt maximal 100.000 Ordner zurück.
seo-description: Gibt alle Ordner und Unterordner ab dem Ordnerpfad zurück. Die getFolders-Antwort gibt maximal 100.000 Ordner zurück.
seo-title: getFolders
solution: Experience Manager
title: getFolders
topic: Scene7 Image Production System API
uuid: 06e9d745-b711-43e3-8dc6-93da66b981b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 8%

---


# getFolders{#getfolders}

Gibt alle Ordner und Unterordner ab dem Ordnerpfad zurück. Die getFolders-Antwort gibt maximal 100.000 Ordner zurück.

## Zweck der Ordner {#section-66e344d5333f42f1b060a0cba25935c3}

Mit einem Ordner können Sie Unterordner und Assets organisieren. Alle Ordner- und Asset-Namen müssen eindeutig sein. Ordner und Assets, die denselben Namen haben, führen zu einem Namensraum-Konflikt, auch wenn sie sich in unterschiedlichen Ordnerhierarchien befinden.
Syntax

## Autorisierte Benutzertypen {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lesezugriff auf den Ordner verfügen, um Daten darauf zurückgeben zu können.

## Parameter {#section-0c1976503eaa418a9226b51667901176}

**Input (getFoldersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| ` *`accessUserHandle`*` | `xsd:string` | Nein | Wird von Administratoren verwendet, um die Identität eines bestimmten Benutzers zu imitieren. |
| ` *`accessGroupHandle`*` | `xsd:string` | Nein | Filtern Sie nach einer bestimmten Gruppe. |
| ` *`folderPath`*` | `xsd:string` | Nein | Der Stammordner zum Abrufen von Ordnern und allen Unterordnern auf Blattebene. Wenn dies ausgeschlossen ist, wird der Stammordner für Firmen verwendet. |
| ` *`assetTypeArray`*` | `types:StringArray` | Nein | Gibt Ordner zurück, die nur bestimmte Asset-Typen enthalten. |
| ` *`responseFieldArray`*` | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie in die Antwort aufnehmen möchten. |
| ` *`excludeFieldArray`*` | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie aus der Antwort ausschließen möchten. |

**Output (getFoldersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`folderArray`*` | `types:FolderArray` | Nein | Ein Array von Ordnern, die den Filterkriterien entsprechen. Die Antwort ist auf maximal 100.000 Ordner beschränkt. |
| ` *`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Beispiele {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Dieses Codebeispiel gibt ein Array zurück, das alle Ordner für eine Firma zusammen mit spezifischen Informationen zu den einzelnen Ordnern enthält.

**Anforderung**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Antwort**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```

