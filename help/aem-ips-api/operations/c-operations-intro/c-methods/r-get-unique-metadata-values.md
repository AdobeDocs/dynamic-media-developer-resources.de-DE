---
description: Ruft eindeutige Metadatenfeldwerte ab.
seo-description: Ruft eindeutige Metadatenfeldwerte ab.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Scene7 Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Ruft eindeutige Metadatenfeldwerte ab.

Syntax

## Autorisierte Benutzertypen {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-b9d1413811c24566b6d095701f0f66db}

**Input (getUniqueMetadataValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| ` *`fieldHandle`*` | `xsd:string` | Nein | Umgang mit dem Metadatenfeld. |

**Output (getUniqueMetadataValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`Werte`*` | `type:StringArray` |  |  |

## Beispiele {#section-440f3bc3e5be436cb6ec26117d05f476}

Dieses Codebeispiel verwendet einen Feldgriff, um bestimmte Metadatenwerte zurückzugeben.

**Anforderung**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Antwort**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

