---
description: Erstellt einen Ordner.
solution: Experience Manager
title: createFolder
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 17%

---


# [!DNL createFolder]{#createfolder}

Erstellt einen Ordner.

>[!NOTE]
>
>Der neue Ordner ist auf den Ordner &quot;Images&quot;Untergeordnet, selbst wenn Sie ein `/` angeben, um den Stammordner der Firma anzugeben.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Die Handhabung der Firma |
| `*`folderPath`*` | `xsd:string` | Ja | Der Stammordner, der zum Abrufen von Ordnern und allen Unterordnern auf Blattebene verwendet wird. Wenn dies ausgeschlossen ist, wird der Stammordner für Firmen verwendet. |

**Output (createFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Ja | Handhabung des neuen Ordners. |

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

