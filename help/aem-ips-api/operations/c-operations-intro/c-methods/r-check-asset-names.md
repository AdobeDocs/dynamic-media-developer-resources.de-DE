---
description: Prüft auf IPS-ID-Konflikte, indem Asset-Namen mit allen Namen im Namespace Image Serving/Image Rendering eines Unternehmens verglichen werden.
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

Prüft auf IPS-ID-Konflikte, indem Asset-Namen mit allen Namen im Namespace Image Serving/Image Rendering eines Unternehmens verglichen werden.

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

**Eingabe (checkAssetNamesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Nein | Das -Handle an die Firma, die den Benutzer enthält. |
| assetNamesArray | `types:StringArray` | Ja | Ein Array von Asset-Namen, die überprüft werden sollen. |

**Ausgabe (checkAssetNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | Ja | Ein Array von Asset-Namen, die verwendet werden. |

## Beispiele {#section-bc5d120d74614a63a425ca3acc337219}

In diesem Beispielcode werden die Asset-Namen angefordert, die für ein bestimmtes Unternehmen verwendet werden. Die Antwort gibt ein Array von Asset-Namen zurück, die verwendet werden.

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
