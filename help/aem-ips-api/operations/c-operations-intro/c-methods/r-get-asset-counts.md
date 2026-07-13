---
description: Ruft die Assets und die Anzahl der mit einem bestimmten Unternehmen verknüpften Assets ab.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 9%

---

# getAssetCounts{#getassetcounts}

Ruft die Assets und die Anzahl der mit einem bestimmten Unternehmen verknüpften Assets ab.

Die zurückgegebene `countArray` besteht aus einem Array von `assetTypes` (Datentyp `xsd:string`) mit jeweils einem eigenen Zählfeld (Datentyp `xsd:int`), sodass mehrere Asset-Typen pro Element des Arrays dargestellt werden können.Syntax

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
| companyHandle | `xsd:string` | Ja | Das Handle für die Firma mit Assets, die Sie zählen möchten. |

**Ausgabe (getAssetCountsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| countArray | `types:AssetCountArray` | Nein | Ein Array von Asset-Typen mit jeweils einem eigenen Zählfeld, das die Darstellung mehrerer Asset-Typen pro Element des Arrays ermöglicht. |

## Beispiele {#section-6052a503eb3843f6adb99e200fdba280}

Dieses Codebeispiel verwendet das -Handle des Unternehmens als Feld in der `getAssetCountsParam`, die an den IPS-Webservice-Server gesendet wird, um die Anzahl der Assets abzurufen.

**Anfrage**

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

