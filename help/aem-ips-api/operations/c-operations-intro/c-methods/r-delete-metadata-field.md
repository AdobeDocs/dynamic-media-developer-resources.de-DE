---
description: Löscht das Metadatenfeld einer Firma.
seo-description: Löscht das Metadatenfeld einer Firma.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Scene7 Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteMetadataField{#deletemetadatafield}

Löscht das Metadatenfeld einer Firma.

Syntax

## Autorisierte Benutzertypen {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-73f12a30cc4340b6b32dd11effd5195e}

**Input (deleteMetadataFieldParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die das zu löschende Metadatenfeld enthält. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Das Handle zum zu löschenden Metadatenfeld. |

**Output (deleteMetadataFieldParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-e1c474ea91a040609ecd7c2400f4fa3c}

In diesem Codebeispiel wird das Metadatenfeld einer Firma gelöscht. Es verwendet den Firmen-Handle und den Metadaten-Handle als Felder in der an den IPS-Webdienstserver `deleteMetadataFieldParam` weitergeleiteten Datei, um diese Aktion auszuführen.

**Anforderung**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Antwort**

None.0
