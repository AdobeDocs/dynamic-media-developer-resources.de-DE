---
description: Gibt ein Array mit Photoshop-Pfadnamen für das angegebene Bild zurück.
solution: Experience Manager
title: getFotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '82'
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

**Eingabe (getFotoshopPathNamesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle mit dem Unternehmen, das das Bild enthält, mit dem Sie arbeiten möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Bild-Asset. |

**Ausgabe (getFotoshopPathNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Ja | Ein Array von Photoshop-Pfadnamen in einem Bild. |

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
