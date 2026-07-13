---
description: Ruft eindeutige Metadatenfeldwerte ab.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
TQID: 'https://experienceleague.adobe.com/iDDSEPmoOHPlfCBx2wN9AEM4xlwC-s6SAPKVDUd6iEk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 24%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

Ruft eindeutige Metadatenfeldwerte ab.

Syntax

## Autorisierte Benutzertypen {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-b9d1413811c24566b6d095701f0f66db}

**Eingabe (getUniqueMetadataValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| fieldHandle | `xsd:string` | Nein | Verarbeiten Sie das -Metadatenfeld. |

**Ausgabe (getUniqueMetadataValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Werte | `type:StringArray` |  |  |

## Beispiele {#section-440f3bc3e5be436cb6ec26117d05f476}

Dieses Codebeispiel verwendet ein Feld-Handle, um bestimmte Metadatenwerte zurückzugeben.

**Anfrage**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Antwort**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

