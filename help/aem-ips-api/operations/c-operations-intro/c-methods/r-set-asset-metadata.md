---
description: Legt Metadatenwerte für ein Asset fest. Funktioniert mit einem Array von Metadatenaktualisierungen, um Werte in einem Batch festzulegen.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
TQID: 'https://experienceleague.adobe.com/b8E8BK8pyJQiYlR2yNMbYPWcLVNfmAvI5WaOBuaBz1E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

Legt Metadatenwerte für ein Asset fest. Funktioniert mit einem Array von Metadatenaktualisierungen, um Werte in einem Batch festzulegen.

Syntax

## Autorisierte Benutzertypen {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lesezugriff auf das Asset haben.

## Parameter {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das -Handle an die Firma mit dem Asset, das Sie aktualisieren möchten. |
| assetHandle | `xsd:string` | Ja | Das Handle zum Asset. |
| updateArray | `types:MetadataUpdateArray` | Ja | Aktualisierungen in einem Metadaten-Update-Array. |

**Ausgabe (setAssetMetadataReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Dieses Codebeispiel verwendet ein Array von Metadatenaktualisierungen, um die Metadaten des angegebenen Assets festzulegen.

**Anfrage**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Antwort**

Keine.
