---
description: Löscht einen Ordner.
seo-description: Löscht einen Ordner.
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
topic: Scene7 Image Production System API
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 11%

---


# deleteFolder{#deletefolder}

Löscht einen Ordner.

Syntax

## Autorisierte Benutzertypen {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lese- und Löschzugriff auf den Ordner und alle untergeordneten Elemente verfügen.

## Parameter {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Input (deleteFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, zu der der Ordner gehört. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Das Handle des zu löschenden Ordners. |

**Output (deleteFolderParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9d4617b322e8442d80e59be0f8714841}

Dieser Beispielcode löscht einen Ordner aus dem Stammordner der Firma. Es ist ein Ordner-Handle erforderlich, das Sie von einem anderen Vorgang abrufen müssen.

**Anforderung**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Keine.
