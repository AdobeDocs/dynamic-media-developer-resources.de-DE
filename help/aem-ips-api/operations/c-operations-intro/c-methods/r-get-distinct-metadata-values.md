---
description: Gibt alle Werte für ein Metadatenfeld zurück.
seo-description: Gibt alle Werte für ein Metadatenfeld zurück.
seo-title: getDistinctMetadataValues
solution: Experience Manager
title: getDistinctMetadataValues
topic: Scene7 Image Production System API
uuid: 47c1d3a3-9f33-4c36-828a-e858370997d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getDistinctMetadataValues{#getdistinctmetadatavalues}

Gibt alle Werte für ein Metadatenfeld zurück.

Syntax

## Autorisierte Benutzertypen {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-600f36a32ff147cb83149943d37843e2}

**Input (getDistinctMetadataValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, für die Sie Daten abrufen möchten. |
| ` *`metadataKey`*` | `xsd:string` | Ja | Metadatenschlüssel in Punktnotation. |

**Output (getDistinctMetadataValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`valueArray`*` | `types:ValueArray` | Ja | Werte des angeforderten Metadatenfelds. |

## Beispiele {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**Anforderung**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Antwort**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

