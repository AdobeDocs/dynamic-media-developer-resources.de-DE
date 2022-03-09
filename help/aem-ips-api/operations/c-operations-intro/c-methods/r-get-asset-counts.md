---
description: Ruft die Assets und die Anzahl der Assets ab, die mit einem bestimmten Unternehmen verknüpft sind.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 10%

---

# getAssetCounts{#getassetcounts}

Ruft die Assets und die Anzahl der Assets ab, die mit einem bestimmten Unternehmen verknüpft sind.

Die `countArray` zurückgegeben wird, besteht aus einem Array von `assetTypes` (Datentyp `xsd:string`), jeweils mit einem eigenen Zählerfeld (Datentyp) `xsd:int`), wodurch mehrere Asset-Typen pro Element des Arrays dargestellt werden können.
Syntax

## Autorisierte Benutzertypen {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Eingabe (getAssetCountsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen mit Assets, die gezählt werden sollen. |

**Ausgabe (getAssetCountsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| countArray | `types:AssetCountArray` | Nein | Ein Array von Asset-Typen mit jeweils einem eigenen Zählerfeld, sodass mehrere Asset-Typen pro Element des Arrays dargestellt werden können. |

## Beispiele {#section-6052a503eb3843f6adb99e200fdba280}

Dieses Codebeispiel verwendet das Handle des Unternehmens als Feld im `getAssetCountsParam` an den IPS-Webdienstserver gesendet werden, um die Asset-Anzahl zu erhalten.

**Anforderung**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Antwort**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```
