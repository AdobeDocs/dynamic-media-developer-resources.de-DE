---
description: Überprüft, ob Konflikte mit IPS-IDs auftreten, indem Asset-Namen mit allen Namen des Namespace des Image Serving/Image Rendering-Katalogs eines Unternehmens verglichen werden.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 11%

---

# checkAssetNames{#checkassetnames}

Überprüft, ob Konflikte mit IPS-IDs auftreten, indem Asset-Namen mit allen Namen des Namespace des Image Serving/Image Rendering-Katalogs eines Unternehmens verglichen werden.

Syntax

## Autorisierte Benutzertypen {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parameter {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Input (checkAssetNamesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Nein | Der Handle für das Unternehmen, das den Benutzer enthält. |
| assetNamesArray | `types:StringArray` | Ja | Ein Array von Asset-Namen, die überprüft werden sollen. |

**Output (checkAssetNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | Ja | Ein Array der verwendeten Asset-Namen. |

## Beispiele {#section-bc5d120d74614a63a425ca3acc337219}

Dieser Beispielcode fordert die Asset-Namen an, die für ein bestimmtes Unternehmen verwendet werden. Die Antwort gibt ein Array von Asset-Namen zurück, die verwendet werden.

**Anfrage**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Antwort**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
