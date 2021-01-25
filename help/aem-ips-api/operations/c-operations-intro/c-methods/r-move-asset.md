---
description: Verschiebt ein Asset in einen bestimmten Ordner.
seo-description: Verschiebt ein Asset in einen bestimmten Ordner.
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Dynamic Media Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 15%

---


# moveAsset{#moveasset}

Verschiebt ein Asset in einen bestimmten Ordner.

Syntax

## Autorisierte Benutzertypen {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Input (moveAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| `*`assetHandle`*` | `xsd:string` | Ja | Handle mit dem Asset, das du verschieben willst. |
| `*`folderHandle`*` | `xsd:string` | Ja | Zum Zielordner gehen. |

**Output (moveAssetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-78333769f4f14e2886fdf06433c9d2ad}

Mit diesem Codebeispiel wird ein Asset in einen Ordner verschoben.

**Anforderung**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Antwort**

Keine.
