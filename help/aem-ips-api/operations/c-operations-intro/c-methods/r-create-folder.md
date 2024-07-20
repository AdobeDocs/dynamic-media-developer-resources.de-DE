---
title: createFolder
description: Erstellt einen Ordner.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 16%

---

# [!DNL createFolder]{#createfolder}

Erstellt einen Ordner.

>[!NOTE]
>
>Der neue Ordner ist dem Ordner Bilder untergeordnet, selbst wenn Sie eine &quot;`/`&quot; angeben, um den Stammordner des Unternehmens anzugeben.

Syntax

## Autorisierte Benutzertypen {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese-/Schreibzugriff auf den übergeordneten Ordner haben.

## Parameter {#section-c00d8d89cf114886a535056f2a1bf892}

**Input (createFolder)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Umgang mit dem Unternehmen |
| folderPath | `xsd:string` | Ja | Der Stammordner, der zum Abrufen von Ordnern und allen Unterordnern auf Blattebene verwendet wird. Wenn diese Option ausgeschlossen ist, wird der Stammordner des Unternehmens verwendet. |

**Output (createFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| folderHandle | `xsd:string` | Ja | Umgang mit dem neuen Ordner. |

## Beispiele {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Dieser Beispielcode erstellt einen Ordner im Stammverzeichnis eines Unternehmens. Die Antwort gibt den Handle des neu erstellten Ordners zurück.

**Anfrage**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Antwort**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
