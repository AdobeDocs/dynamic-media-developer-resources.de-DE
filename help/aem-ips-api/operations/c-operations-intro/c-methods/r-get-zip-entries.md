---
description: Gibt Zip-Dateidaten zurück.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 20%

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
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen, das die Zip-Datei enthält. |
| assetHandle | `xsd:string` | Ja | Bearbeiten Sie die ZIP-Datei. |

**Output (getZipEntriesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| zipArray | `types:ZipEntryArray` | Ja | Array von Einträgen in einer Zip-Datei. |

## Beispiele {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Dieses Codebeispiel gibt Informationen zur Postleitzahl zurück, einschließlich der komprimierten und unkomprimierten Größe.

**Anfrage**

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
