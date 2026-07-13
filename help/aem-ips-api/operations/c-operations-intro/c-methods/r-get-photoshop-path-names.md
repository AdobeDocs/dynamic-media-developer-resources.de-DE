---
description: Gibt ein Array von Photoshop-Pfadnamen für das jeweilige Bild zurück.
solution: Experience Manager
title: getFotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
TQID: 'https://experienceleague.adobe.com/BxFBNXpa9ilc4lXeXiuuvCQb9ChImZWt13-pJ3b3osk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 18%

---

# getFotoshopPathNames{#getphotoshoppathnames}

Gibt ein Array von Photoshop-Pfadnamen für das jeweilige Bild zurück.

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
| companyHandle | `xsd:string` | Ja | Übergeben Sie an die Firma, die das Bild enthält, mit dem Sie arbeiten möchten. |
| assetHandle | `xsd:string` | Ja | Verarbeiten Sie das Bild-Asset. |

**Ausgabe (getFotoshopPathNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| pathNameArray | `types:StringArray` | Ja | Ein Array von Photoshop-Pfadnamen in einem Bild. |

## Beispiele {#section-6d316f14b4184d42af4ca3f717b042dd}

**Anfrage**

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

