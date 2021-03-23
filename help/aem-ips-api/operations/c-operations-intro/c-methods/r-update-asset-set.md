---
description: Aktualisiert einen Asset-Satz.
seo-description: Aktualisiert einen Asset-Satz.
seo-title: updateAssetSet
solution: Experience Manager
title: updateAssetSet
uuid: e844a395-0ab3-45a7-bcec-8e9e15efc70e
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 18%

---


# updateAssetSet{#updateassetset}

Aktualisiert einen Asset-Satz.

Syntax

## Parameter {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, die den Bildsatz enthält, den Sie ändern möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Der Griff zum Bildsatz, den Sie ändern möchten. |
| `*`setDefinition`*` | `xsd:string` | Nein | Setzt Bildsatzmitglieder zurück. |
| `*`thumbAssetHandle`*` | `xsd:string` | Nein | Das Handle des Assets, das als Miniaturansicht für den Bildsatz fungiert. |

**Output (updateAssetSetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
|  |  |  |  |

## Beispiele {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Anforderung**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Antwort**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

