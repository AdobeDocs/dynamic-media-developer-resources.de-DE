---
description: Gibt Koordinaten für die quadrilaterale Ebene zurück, die den benannten Fotoshop-Pfad einschließen.
seo-description: Gibt Koordinaten für die quadrilaterale Ebene zurück, die den benannten Fotoshop-Pfad einschließen.
seo-title: getFotoshopPath
solution: Experience Manager
title: getFotoshopPath
topic: Scene7 Image Production System API
uuid: e3ed4888-18db-40bc-a1db-f44a342d0293
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# getFotoshopPath{#getphotoshoppath}

Gibt Koordinaten für die quadrilaterale Ebene zurück, die den benannten Fotoshop-Pfad einschließen.

Syntax

## Autorisierte Benutzertypen {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* ``

## Parameter {#section-ebffe496284c4ced9f329f78127be199}

**Input (getFotoshopPathParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Nehmen Sie die Firma mit dem Bild, mit dem Sie arbeiten möchten. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Bild-Asset. |
| ` *`pathName`*` | `xsd:string` | Ja | Name des Fotoshop-Pfads, den Sie zurückgeben möchten. |

**Output (getFotoshopPathReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`perspectiveQuad`*` | `types:PerspectiveQuad` | Ja | Gibt Bildkoordinaten basierend auf dem Pfad zurück. Siehe [PerectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

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

