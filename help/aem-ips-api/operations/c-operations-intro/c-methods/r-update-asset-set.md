---
description: Aktualisiert einen Asset-Satz.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 22%

---

# updateAssetSet{#updateassetset}

Aktualisiert einen Asset-Satz.

Syntax

## Parameter {#section-d7080ccd97334c94860eb107a3e132b2}

**Eingabe (updateAssetSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das zu ändernde Bildset enthält. |
| assetHandle | `xsd:string` | Ja | Das Handle für das Bildset, das Sie ändern möchten. |
| setDefinition | `xsd:string` | Nein | Setzt Bildset-Mitglieder zurück. |
| thumbAssetHandle | `xsd:string` | Nein | Der Handle des Assets, das als Miniaturansicht für das Bildset dient. |

**Ausgabe (updateAssetSetReturn)**

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
