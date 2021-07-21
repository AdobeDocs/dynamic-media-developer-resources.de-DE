---
description: Löscht einen Ordner.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 10%

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
>Der Benutzer muss Lese- und Löschzugriff auf den Ordner und alle seine untergeordneten Elemente haben.

## Parameter {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Eingabe (deleteFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle des Unternehmens, zu dem der Ordner gehört. |
| `*`folderHandle`*` | `xsd:string` | Ja | Der Handle für den Ordner, der gelöscht werden soll. |

**Ausgabe (deleteFolderParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9d4617b322e8442d80e59be0f8714841}

Mit diesem Beispielcode wird ein Ordner aus dem Stammverzeichnis des Unternehmens gelöscht. Dazu ist ein Ordner-Handle erforderlich, das Sie von einem anderen Vorgang abrufen müssen.

**Anforderung**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Keine.
