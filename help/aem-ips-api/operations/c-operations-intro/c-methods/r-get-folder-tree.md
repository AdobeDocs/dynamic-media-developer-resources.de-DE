---
description: Gibt Ordner und Unterordner in einer hierarchischen Baumstruktur zurück. Die Antwort von „getFolderTree“ ist auf maximal 100.000 Ordner beschränkt
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# getFolderTree{#getfoldertree}

Gibt Ordner und Unterordner in einer hierarchischen Baumstruktur zurück. Die Antwort von „getFolderTree“ ist auf maximal 100.000 Ordner beschränkt

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
>Der Benutzer muss über Lesezugriff auf den Ordner verfügen, um Daten darüber zurückzugeben.

## Parameter {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Eingabe (getFolderTreeParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen. |
| accessUserHandle | `xsd:string` | Nein | Wird nur von Administratoren verwendet, um die Identität eines bestimmten Benutzers zu übernehmen. |
| accessGroupHandle | `xsd:string` | Nein | Wird zum Filtern nach einer bestimmten Gruppe verwendet, einschließlich derjenigen, zu denen das Unternehmen gehört. |
| folderPath | `xsd:string` | Nein | Der Stammordner zum Abrufen von Ordnern und allen Unterordnern auf Blattebene. Wenn dies ausgeschlossen ist, wird der Stammordner des Unternehmens verwendet. |
| Tiefe | `xsd:int` | Ja | Bei einem Wert von null wird der Ordner der obersten Ebene abgerufen. Jeder andere Wert gibt die Tiefe an, die in die Baumstruktur abgesenkt werden soll. |
| assetTypeArray | `types:StringArray` | Nein | Gibt Ordner zurück, die nur angegebene Asset-Typen enthalten. |
| responseFieldArray | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie in die Antwort aufnehmen möchten. |
| excludeFieldArray | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie in der Antwort ausschließen möchten. |

**Ausgabe (getFolderTreeReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Ordner | `types:folders` | Nein | Die Ordnerhierarchie in einer Baumstruktur. Die Antwort ist auf maximal 100.000 Ordner beschränkt. |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## Beispiele {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

In diesem Code-Beispiel werden ein Firmen-Handle und ein Tiefenparameter verwendet, um die Tiefe zu bestimmen, die die Antwort zurückgeben soll. Die Antwort enthält Ordner und Unterordner-Arrays mit verwandten Ordnern. Legen Sie für den Tiefenwert eine kleinere Zahl fest, um tiefer in der Ordnerstruktur zu suchen.

**Anfrage**

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
