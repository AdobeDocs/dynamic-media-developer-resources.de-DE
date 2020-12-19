---
description: Gibt Zip-Dateidaten zurück.
seo-description: Gibt Zip-Dateidaten zurück.
seo-title: getZipEntries
solution: Experience Manager
title: getZipEntries
topic: Scene7 Image Production System API
uuid: cfc45f83-1cf9-4c50-9aac-5a731e62a839
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 21%

---


# getZipEntries{#getzipentries}

Gibt Zip-Dateidaten zurück.

Syntax

## Autorisierte Benutzertypen {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Input (getZipEntriesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die die Zip-Datei enthält. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Behandeln Sie die Zip-Datei. |

**Output (getZipEntriesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`zipArray`*` | `types:ZipEntryArray` | Ja | Array von Einträgen in einer Zip-Datei. |

## Beispiele {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Dieses Codebeispiel gibt Zip-Dateiinformationen zurück, einschließlich komprimierter und unkomprimierter Größe.

**Anforderung**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Antwort**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

