---
description: Gibt alle Metadatenfelder zurück, gruppiert nach Asset-Typ.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic, SDK/API, Metadaten, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 20%

---


# getAssetMetadataFields{#getassetmetadatafields}

Gibt alle Metadatenfelder zurück, gruppiert nach Asset-Typ.

Syntax

## Autorisierte Benutzertypen {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Input (getAssetMetadataFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, deren Metadaten Sie abrufen möchten. |

**Output (getAssetMetadataFieldsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Ja | Array von Metadatenfeldern nach Asset-Typ. |

## Beispiele {#section-d79ab85f29144635b0b61416e52f4f3f}

**Anforderung**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Antwort**

>[!NOTE]
>
>Kürzlich wegen der Kürze.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

