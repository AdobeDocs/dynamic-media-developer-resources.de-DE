---
description: Ruft die Assets und die Anzahl der Assets ab, die mit einer bestimmten Firma verknüpft sind.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---


# getAssetCounts{#getassetcounts}

Ruft die Assets und die Anzahl der Assets ab, die mit einer bestimmten Firma verknüpft sind.

Das zurückgegebene `countArray` besteht aus einem Array von `assetTypes` (Datentyp `xsd:string`), von denen jedes über ein eigenes Zählfeld (Datentyp `xsd:int`) verfügt, sodass mehrere Asset-Typen pro Element des Arrays angezeigt werden können.
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
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle zur Firma mit den Elementen, die gezählt werden sollen. |

**Output (getAssetCountsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | Nein | Ein Array von Asset-Typen mit jeweils einem eigenen Zählfeld, das die Darstellung mehrerer Asset-Typen pro Element des Arrays ermöglicht. |

## Beispiele {#section-6052a503eb3843f6adb99e200fdba280}

Dieses Codebeispiel verwendet das Handle der Firma als Feld im Feld `getAssetCountsParam`, das an den IPS-Webdienstserver gesendet wird, um die Asset-Zählung abzurufen.

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

