---
description: Prüft auf IPS-ID-Konflikte, indem Asset-Namen mit allen Namen eines Image Serving-/Image Rendering-Katalogs einer Firma verglichen werden.
seo-description: Prüft auf IPS-ID-Konflikte, indem Asset-Namen mit allen Namen eines Image Serving-/Image Rendering-Katalogs einer Firma verglichen werden.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Scene7 Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkAssetNames{#checkassetnames}

Prüft auf IPS-ID-Konflikte, indem Asset-Namen mit allen Namen eines Image Serving-/Image Rendering-Katalogs einer Firma verglichen werden.

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
| ` *`companyHandle`*` | `xsd:string` | Nein | Das Handle der Firma, in der sich der Benutzer befindet. |
| ` *`assetNamesArray`*` | `types:StringArray` | Ja | Ein Array mit zu prüfenden Asset-Namen. |

**Output (checkAssetNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`inUseNameArray`*` | `types:StringArray` | Ja | Ein Array mit den verwendeten Asset-Namen. |

## Beispiele {#section-bc5d120d74614a63a425ca3acc337219}

Dieser Beispielcode fordert die Namen der Assets an, die für eine bestimmte Firma verwendet werden. Die Antwort gibt ein Array von Asset-Namen zurück, die verwendet werden.

**Anforderung**

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

