---
description: Verschiebt ein Asset in einen bestimmten Ordner.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 14%

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

**Eingabe (moveAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| assetHandle | `xsd:string` | Ja | Verarbeiten Sie das Asset, das Sie verschieben möchten. |
| folderHandle | `xsd:string` | Ja | Verarbeiten Sie den Zielordner. |

**Ausgabe (moveAssetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-78333769f4f14e2886fdf06433c9d2ad}

Dieses Code-Beispiel verschiebt ein Asset in einen Ordner.

**Anfrage**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Antwort**

Keine.
