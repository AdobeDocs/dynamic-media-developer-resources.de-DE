---
description: Gibt Koordinaten für die quadrilaterale Darstellung des benannten Photoshop-Pfads zurück.
solution: Experience Manager
title: getFotoshopPath
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 18%

---


# getFotoshopPath{#getphotoshoppath}

Gibt Koordinaten für die quadrilaterale Darstellung des benannten Photoshop-Pfads zurück.

Syntax

## Autorisierte Benutzertypen {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parameter {#section-ebffe496284c4ced9f329f78127be199}

**Input (getFotoshopPathParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Nehmen Sie die Firma mit dem Bild, mit dem Sie arbeiten möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Bild-Asset. |
| `*`pathName`*` | `xsd:string` | Ja | Name des Photoshop-Pfads, den Sie zurückgeben möchten. |

**Output (getFotoshopPathReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`perspectiveQuad`*` | `types:PerspectiveQuad` | Ja | Gibt Bildkoordinaten basierend auf dem Pfad zurück. Siehe [PerectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Beispiele {#section-1f0461cbdc184c8d8925336d5279db47}

**Anforderung**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Antwort**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

