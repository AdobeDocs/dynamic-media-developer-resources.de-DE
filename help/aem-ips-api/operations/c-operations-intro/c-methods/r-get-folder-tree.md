---
description: Gibt Ordner und Unterordner in einer hierarchischen Baumstruktur zurück. Die getFolderTree-Antwort ist auf maximal 100.000 Ordner beschränkt
seo-description: Gibt Ordner und Unterordner in einer hierarchischen Baumstruktur zurück. Die getFolderTree-Antwort ist auf maximal 100.000 Ordner beschränkt
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
topic: Scene7 Image Production System API
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 8%

---


# getFolderTree{#getfoldertree}

Gibt Ordner und Unterordner in einer hierarchischen Baumstruktur zurück. Die getFolderTree-Antwort ist auf maximal 100.000 Ordner beschränkt

Syntax

## Autorisierte Benutzertypen {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lesezugriff auf den Ordner verfügen, um Daten darauf zurückgeben zu können.

## Parameter {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Input (getFolderTreeParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| ` *`accessUserHandle`*` | `xsd:string` | Nein | Wird nur von Administratoren verwendet, um die Identität eines bestimmten Benutzers zu imitieren. |
| ` *`accessGroupHandle`*` | `xsd:string` | Nein | Dient zum Filtern nach einer bestimmten Gruppe, einschließlich derjenigen, zu denen die Firma gehört. |
| ` *`folderPath`*` | `xsd:string` | Nein | Der Stammordner zum Abrufen von Ordnern und allen Unterordnern auf Blattebene. Wenn dies ausgeschlossen ist, wird der Stammordner für Firmen verwendet. |
| ` *`Tiefe`*` | `xsd:int` | Ja | Der Wert null ruft den Ordner der obersten Ebene ab. Jeder andere Wert gibt die Tiefe an, die in den Baum absinkt. |
| ` *`assetTypeArray`*` | `types:StringArray` | Nein | Gibt Ordner zurück, die nur bestimmte Asset-Typen enthalten. |
| ` *`responseFieldArray`*` | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie in die Antwort aufnehmen möchten. |
| ` *`excludeFieldArray`*` | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie in der Antwort ausschließen möchten. |

**Output (getFolderTreeReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`Ordner`*` | `types:folders` | Nein | Die Hierarchie der Ordner in einer Baumstruktur. Die Antwort ist auf maximal 100.000 Ordner beschränkt. |
| ` *`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Beispiele {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Dieses Codebeispiel verwendet einen Firma-Handle und einen Tiefenstufe-Parameter, um die Tiefe zu bestimmen, die die Antwort zurückgeben soll. Die Antwort enthält Ordner und Unterordner-Arrays mit zugehörigen Elementen. Stellen Sie den Wert für die Tiefe auf eine kleinere Zahl ein, um tiefer in die Ordnerstruktur zu suchen.

**Anforderung**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Antwort**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```

