---
description: Gibt ein Array mit Photoshop-Pfadnamen für das angegebene Bild zurück.
solution: Experience Manager
title: getFotoshopPathNames
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 19%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Nehmen Sie die Firma mit dem Bild vor, mit dem Sie arbeiten möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Bild-Asset. |

**Output (getFotoshopPathNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Ja | Ein Array mit Photoshop-Pfadnamen in einem Bild. |

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

