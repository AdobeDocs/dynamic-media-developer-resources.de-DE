---
description: Löscht ein Bildformat. Rufen Sie das Format-Handle von saveImageFormat ab.
seo-description: Löscht ein Bildformat. Rufen Sie das Format-Handle von saveImageFormat ab.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Scene7 Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteImageFormat{#deleteimageformat}

Löscht ein Bildformat. Rufen Sie das Format-Handle von saveImageFormat ab.

Syntax

## Autorisierte Benutzertypen {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-462c05d9aad746ee8d2be0656041b693}

**Input (deleteImageFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die das zu löschende Bildformat enthält. |
| ` *`imageFormatHandle`*` | `xsd:string` | Ja | Der Griff zum Bildformat, das Sie löschen möchten. |

**Output (deleteImageFormatParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Dieses Codebeispiel löscht ein Bildformat aus einer Firma. Rufen Sie den Bildformatgriff von einem anderen Vorgang ab.

**Anforderung**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Antwort**

Keine.

**Verwandtes Thema:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
