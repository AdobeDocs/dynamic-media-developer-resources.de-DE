---
description: Löscht einen Ordner.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
TQID: 'https://experienceleague.adobe.com/OfZbcMyLmLvg6x088Y5y0DBM7-C--jW7oPtOfIaSwDk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 96
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
>Der Benutzer muss Lese- und Löschzugriff auf den Ordner und alle untergeordneten Elemente haben.

## Parameter {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Input (deleteFolderParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle des Unternehmens, zu dem der Ordner gehört. |
| folderHandle | `xsd:string` | Ja | Der Handle zum zu löschenden Ordner. |

**Ausgabe (deleteFolderParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9d4617b322e8442d80e59be0f8714841}

Dieser Beispielcode löscht einen Ordner aus dem Stammverzeichnis des Unternehmens. Dazu ist ein Ordner-Handle erforderlich, das Sie von einem anderen Vorgang erhalten müssen.

**Anfrage**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Keine.

