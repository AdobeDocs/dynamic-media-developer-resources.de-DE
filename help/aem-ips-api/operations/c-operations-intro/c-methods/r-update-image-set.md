---
description: Aktualisiert einen Bildsatz.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 18%

---


# updateImageSet{#updateimageset}

Aktualisiert einen Bildsatz.

Syntax

## Parameter {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, die den Bildsatz enthält, den Sie ändern möchten. |
| `*`assetHandle`*` | `xsd:string` | Ys | Der Griff zum Bildsatz, den Sie ändern möchten. |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | Nein | Setzt Bildsatzmitglieder zurück. |
| `*`thumbAssetHandle`*` | `xsd:string` | Nein | Das Handle des Assets, das als Miniaturansicht für den Bildsatz fungiert. |

**Output (updateImageSetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`Sequenz`*` |  |  |  |

## Beispiele {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Anforderung**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Antwort**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

