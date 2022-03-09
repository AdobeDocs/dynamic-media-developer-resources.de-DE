---
description: Ruft die benutzerdefinierten Metadatenfelder ab, die mit einem Asset verknüpft sind.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 15%

---

# getMetadataFields{#getmetadatafields}

Ruft die benutzerdefinierten Metadatenfelder ab, die mit einem Asset verknüpft sind.

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

**Eingabe (getMetadataFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle des Unternehmens. |
| assetType | `xsd:string` | Ja | Asset-Typen, aus denen Metadaten abgerufen werden sollen. |

**Ausgabe (getMetadataFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Codeausdruck | `Code Phrase` |  |  |

## Beispiele {#section-dbfde1483d614b5aac2b491cb32115d7}

Dieses Codebeispiel gibt Metadaten-Assets für den angegebenen Typ und das angegebene Unternehmen zurück. Die Antwort enthält ein Array von Metadatenfeldern in einem Feld-Array. Nicht alle Assets verfügen über dieselben Metadaten. Der IPS-Benutzer definiert das Metadatenfeld des Assets.

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
