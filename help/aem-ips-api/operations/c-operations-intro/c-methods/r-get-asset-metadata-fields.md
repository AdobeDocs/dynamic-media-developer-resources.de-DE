---
description: Gibt alle Metadatenfelder gruppiert nach Asset-Typ zurück.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---

# getAssetMetadataFields{#getassetmetadatafields}

Gibt alle Metadatenfelder gruppiert nach Asset-Typ zurück.

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

**Eingabe (getAssetMetadataFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, dessen Metadaten Sie abrufen möchten. |

**Ausgabe (getAssetMetadataFieldsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Ja | Array von Metadatenfeldern, nach Asset-Typ. |

## Beispiele {#section-d79ab85f29144635b0b61416e52f4f3f}

**Anfrage**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Antwort**

>[!NOTE]
>
>Aus Gründen der Kürze gekürzt

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
