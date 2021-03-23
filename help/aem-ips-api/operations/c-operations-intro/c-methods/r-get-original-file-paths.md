---
description: Ruft die ursprünglichen Dateipfade der Assets einer Firma ab.
seo-description: Ruft die ursprünglichen Dateipfade der Assets einer Firma ab.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
uuid: c4acf288-1a57-4295-806b-348f15a089cc
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 13%

---


# getOriginalFilePaths{#getoriginalfilepaths}

Ruft die ursprünglichen Dateipfade der Assets einer Firma ab.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Array von Handles zu Assets, deren ursprünglicher Dateipfad Sie abrufen möchten. |

**Output (getOriginalFilePathsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | Ja | Das Array von Zeichenfolgen, die die ursprünglichen Dateipfade darstellen. |

## Beispiele {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Dieses Codebeispiel gibt die Dateipfade von Assets zurück, die mit eindeutigen Asset-Handles in einem Asset-Handle-Array angegeben wurden.

**Anforderung**

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

