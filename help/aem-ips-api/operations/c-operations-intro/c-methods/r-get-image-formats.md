---
description: Gibt Bildformate wie PDF, EPS, SWF und andere zurück.
seo-description: Gibt Bildformate wie PDF, EPS, SWF und andere zurück.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Scene7 Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageFormats{#getimageformats}

Gibt Bildformate wie PDF, EPS, SWF und andere zurück.

Syntax

## Autorisierte Benutzertypen {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input (getImageFormatsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit den Bildformaten, die Sie abrufen möchten. |

**Output (getImageFormatsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`imageFormatArray`*` | `types:ImageFormatArray` | Ja | Das Bildformat-Array. |

## Beispiele {#section-73881e12839b4904bf3299b0920bdd0c}

Dieses Codebeispiel gibt alle Bildformate für die angegebene Firma zurück.

**Anforderung**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Antwort**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

