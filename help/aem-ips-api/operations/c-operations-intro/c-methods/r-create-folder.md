---
description: Erstellt einen Ordner.
seo-description: Erstellt einen Ordner.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: d64337d3ed7bd78c681c3022cda20012726d7ccc
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 20%

---


# [!DNL createFolder]{#createfolder}

Erstellt einen Ordner.

>[!NOTE]
>
>Der neue Ordner ist dem Ordner &quot;Images&quot;untergeordnet, auch wenn Sie einen Ordner angeben, `/` der den Stammordner der Firma angibt.

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Die Handhabung der Firma |
| ` *`folderPath`*` | `xsd:string` | Ja | Der Stammordner, der zum Abrufen von Ordnern und allen Unterordnern auf Blattebene verwendet wird. Wenn dies ausgeschlossen ist, wird der Stammordner für Firmen verwendet. |

**Output (createFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Ja | Handhabung des neuen Ordners. |

## Beispiele {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Mit diesem Beispielcode wird ein Ordner im Stammordner einer Firma erstellt. Die Antwort gibt den Handle des neu erstellten Ordners zurück.

**Anforderung**

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

