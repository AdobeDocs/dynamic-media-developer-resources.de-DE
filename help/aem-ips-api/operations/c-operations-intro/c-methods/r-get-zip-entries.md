---
description: Gibt ZIP-Dateidaten zurück.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
TQID: 'https://experienceleague.adobe.com/-fb25TjtmLMUiZe8gRLz7QmtajqVKASUwwc6TQfjN48'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 20%

---

# getZipEntries{#getzipentries}

Gibt ZIP-Dateidaten zurück.

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

**Eingabe (getZipEntriesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das -Handle an das Unternehmen, das die ZIP-Datei enthält. |
| assetHandle | `xsd:string` | Ja | Verarbeiten Sie die ZIP-Datei. |

**Ausgabe (getZipEntriesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| zipArray | `types:ZipEntryArray` | Ja | Array von Einträgen in einer ZIP-Datei. |

## Beispiele {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Dieses Codebeispiel gibt ZIP-Dateiinformationen zurück, einschließlich komprimierter und unkomprimierter Größe.

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
