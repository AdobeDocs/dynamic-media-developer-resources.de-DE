---
description: Ruft die Assets und die Anzahl der Assets ab, die mit einer bestimmten Firma verknüpft sind.
seo-description: Ruft die Assets und die Anzahl der Assets ab, die mit einer bestimmten Firma verknüpft sind.
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
topic: Scene7 Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetCounts{#getassetcounts}

Ruft die Assets und die Anzahl der Assets ab, die mit einer bestimmten Firma verknüpft sind.

Das `countArray` zurückgegebene Element besteht aus einem Array von `assetTypes` (Datentyp `xsd:string`), von denen jeder über ein eigenes Zählfeld (Datentyp `xsd:int`) verfügt, sodass mehrere Asset-Typen pro Element des Arrays dargestellt werden können.
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

**Input (getAssetCountsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle zur Firma mit den Elementen, die gezählt werden sollen. |

**Output (getAssetCountsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`countArray`*` | `types:AssetCountArray` | Nein | Ein Array von Asset-Typen mit jeweils einem eigenen Zählfeld, das die Darstellung mehrerer Asset-Typen pro Element des Arrays ermöglicht. |

## Beispiele {#section-6052a503eb3843f6adb99e200fdba280}

Dieses Codebeispiel verwendet das Handle der Firma als Feld in der an den IPS-Webdienstserver `getAssetCountsParam` gesendeten Datei, um die Elementanzahl abzurufen.

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

