---
description: Ruft die mit einem Asset verknüpften benutzerdefinierten Metadatenfelder ab.
seo-description: Ruft die mit einem Asset verknüpften benutzerdefinierten Metadatenfelder ab.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
topic: Scene7 Image Production System API
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getMetadataFields{#getmetadatafields}

Ruft die mit einem Asset verknüpften benutzerdefinierten Metadatenfelder ab.

Syntax

## Autorisierte Benutzertypen {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-bac949e59c0546429c5786fe422d750d}

**Input (getMetadataFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma. |
| ` *`assetType`*` | `xsd:string` | Ja | Asset-Typen, aus denen Metadaten abgerufen werden. |

**Output (getMetadataFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`Codebegriff`*` | `Code Phrase` |  |  |

## Beispiele {#section-dbfde1483d614b5aac2b491cb32115d7}

Dieses Codebeispiel gibt Metadaten-Assets für den angegebenen Typ und die angegebene Firma zurück. Die Antwort enthält ein Array von Metadatenfeldern in einem Feldarray. Nicht alle Assets haben die gleichen Metadaten. Der IPS-Benutzer definiert das Metadatenfeld des Assets.

**Anforderung**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Antwort**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

