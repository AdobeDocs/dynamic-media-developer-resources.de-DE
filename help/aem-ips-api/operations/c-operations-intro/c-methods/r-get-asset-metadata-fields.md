---
description: Gibt alle Metadatenfelder zurück, gruppiert nach Asset-Typ.
seo-description: Gibt alle Metadatenfelder zurück, gruppiert nach Asset-Typ.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Dynamic Media Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
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

