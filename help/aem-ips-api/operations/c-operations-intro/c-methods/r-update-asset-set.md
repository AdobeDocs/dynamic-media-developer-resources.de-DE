---
description: Aktualisiert einen Asset-Satz.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
TQID: 'https://experienceleague.adobe.com/D74n9esGrb36fQcp35KsbB2DNEuddDt4EaKTH4uLlek'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 19%

---

# updateAssetSet{#updateassetset}

Aktualisiert einen Asset-Satz.

Syntax

## Parameter {#section-d7080ccd97334c94860eb107a3e132b2}

**Eingabe (updateAssetSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das Bildset enthält, das Sie ändern möchten. |
| assetHandle | `xsd:string` | Ja | Das Handle für das Bildset, das Sie ändern möchten. |
| setDefinition | `xsd:string` | Nein | Setzt die Mitglieder des Bildsets zurück. |
| thumbAssetHandle | `xsd:string` | Nein | Das Handle des Assets, das als Miniatur für das Bildset fungiert. |

**Ausgabe (updateAssetSetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
|   |  |  |  |

## Beispiele {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Anfrage**

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
