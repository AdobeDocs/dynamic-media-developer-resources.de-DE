---
description: Gibt ein Array mit Photoshop-Pfadnamen für das angegebene Bild zurück.
seo-description: Gibt ein Array mit Photoshop-Pfadnamen für das angegebene Bild zurück.
seo-title: getFotoshopPathNames
solution: Experience Manager
title: getFotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 17%

---


# getFotoshopPathNames{#getphotoshoppathnames}

Gibt ein Array mit Photoshop-Pfadnamen für das angegebene Bild zurück.

Syntax

## Autorisierte Benutzertypen {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-605a4aab23104489a21f7f7f5849801b}

**Input (getFotoshopPathNamesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Nehmen Sie die Firma mit dem Bild vor, mit dem Sie arbeiten möchten. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Bild-Asset. |

**Output (getFotoshopPathNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | Ja | Ein Array mit Photoshop-Pfadnamen in einem Bild. |

## Beispiele {#section-6d316f14b4184d42af4ca3f717b042dd}

**Anforderung**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Antwort**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

