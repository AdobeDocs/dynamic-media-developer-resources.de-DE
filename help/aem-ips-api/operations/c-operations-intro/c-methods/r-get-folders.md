---
description: Gibt alle Ordner und Unterordner ausgehend vom Ordnerpfad aus zurück. Die getFolders-Antwort gibt maximal 100.000 Ordner zurück.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 7%

---

# getFolders{#getfolders}

Gibt alle Ordner und Unterordner ausgehend vom Ordnerpfad aus zurück. Die getFolders-Antwort gibt maximal 100.000 Ordner zurück.

## Zweck der Ordner {#section-66e344d5333f42f1b060a0cba25935c3}

Mit einem Ordner können Sie Unterordner und Assets organisieren. Alle Ordner- und Asset-Namen müssen eindeutig sein. Ordner und Assets mit demselben Namen verursachen einen Namespace-Konflikt, auch wenn sie sich in unterschiedlichen Ordnerhierarchien befinden.
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
>Der Benutzer muss über Lesezugriff auf den Ordner verfügen, um Daten darüber zurückzugeben.

## Parameter {#section-0c1976503eaa418a9226b51667901176}

**Eingabe (getFoldersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen. |
| accessUserHandle | `xsd:string` | Nein | Wird von Administratoren verwendet, um die Identität eines bestimmten Benutzers auszudrücken. |
| accessGroupHandle | `xsd:string` | Nein | Nach einer bestimmten Gruppe filtern. |
| folderPath | `xsd:string` | Nein | Der Stammordner zum Abrufen von Ordnern und allen Unterordnern auf Blattebene. Wenn dies ausgeschlossen ist, wird der Stammordner des Unternehmens verwendet. |
| assetTypeArray | `types:StringArray` | Nein | Gibt Ordner zurück, die nur angegebene Asset-Typen enthalten. |
| responseFieldArray | `types:StringArray` | Nein | Enthält eine Liste von Feldern, die Sie in die Antwort aufnehmen möchten. |
| excludeFieldArray | `types:StringArray` | Nein | Enthält eine Liste der Felder, die Sie aus der Antwort ausschließen möchten. |

**Ausgabe (getFoldersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| folderArray | `types:FolderArray` | Nein | Ein Array von Ordnern, die den Filterkriterien entsprechen. Die Antwort ist auf maximal 100.000 Ordner beschränkt. |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## Beispiele {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Dieses Codebeispiel gibt ein -Array zurück, das alle Ordner für ein Unternehmen zusammen mit spezifischen Informationen zu den einzelnen Ordnern enthält.

**Anfrage**

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
