---
description: Erstellt ein Bildset.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
TQID: 'https://experienceleague.adobe.com/os4DfkGa5cTZfMN1vc5HeA8Qvauvwb5Q0dZ2P3HFI-c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 13%

---

# createImageSet{#createimageset}

Erstellt ein Bildset.

Syntax

## Autorisierte Benutzertypen {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Die Benutzerin bzw. der Benutzer muss Lese-/Schreibzugriff auf den Zielordner haben.

## Parameter {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, zu dem das Bildset gehört. |
| folderHandle | `xsd:string` | Ja | Der Handle zum Ordner. |
| name | `xsd:string` | Ja | Name des Bildsets. |
| Typ | `xsd:string` | Ja | Typ des Bildsets. |
| thumbAssetHandle | `xsd:string` | Nein | Handle des Assets, das als Miniatur für das neue Bildset fungiert. Wenn kein Wert angegeben ist, versucht IPS, das erste Bild-Asset zu verwenden, auf das vom Set verwiesen wird. |

**Ausgabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Der Ziehpunkt zum neuen Bildset. |

## Beispiele {#section-385fe3b0af8044b0a2451336ec137fc5}

Dieses Codebeispiel erstellt ein Bildset, das durch Firma, Ordner, Name und Typ angegeben wird. Die Antwort ist ein Asset-Handle des neu erstellten Bildsets.

**Anfrage**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Antwort**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
