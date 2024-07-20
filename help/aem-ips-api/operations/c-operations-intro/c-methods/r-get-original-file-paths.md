---
description: Ruft die ursprünglichen Dateipfade der Assets eines Unternehmens ab.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 14%

---

# getOriginalFilePaths{#getoriginalfilepaths}

Ruft die ursprünglichen Dateipfade der Assets eines Unternehmens ab.

Syntax

## Autorisierte Benutzertypen {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Erfordert Lesezugriff auf das Asset.

## Parameter {#section-a6b394daba6e49a8882cf3051035d9d1}

**Input (getOriginalFilePathsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen. |
| assetHandleArray | `types:HandleArray` | Ja | Array von Handles zu Assets, deren ursprünglichen Dateipfad Sie abrufen möchten. |

**Output (getOriginalFilePathsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| originalFileArray | `types:StringArray` | Ja | Das Array von Zeichenfolgen, die die ursprünglichen Dateipfade darstellen. |

## Beispiele {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Dieses Codebeispiel gibt die Dateipfade von Assets zurück, die mit eindeutigen Asset-Handles in einem Asset-Handle-Array angegeben wurden.

**Anfrage**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Antwort**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```
