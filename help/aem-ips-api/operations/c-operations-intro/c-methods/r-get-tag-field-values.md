---
description: Ruft alle Tag-Wörterbuchwerte ab, die für ein oder mehrere Tag-Felder definiert sind.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 16%

---

# getTagFieldValues{#gettagfieldvalues}

Ruft alle Tag-Wörterbuchwerte ab, die für ein oder mehrere Tag-Felder definiert sind.

Syntax

## Autorisierte Benutzertypen {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-9ad806e7736e4d51ae42cad185050cf9}

**Input (getTagFieldValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle des Unternehmens, das das Tag-Feld enthält. |
| fieldHandleArray | `types:HandleArray` | Ja | Ein Array von Feld-Handles zum Taggen von Werten, die zurückgegeben werden sollen. |

**Output (getTagFieldValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| fieldArray | `types:TagFieldValuesArray` | Ja | Ein Array der Tag-Werte im Wörterbuch für jedes angeforderte Feld. |

## Beispiele {#section-4492742614e44bb191a7d397dc1a1407}

**Anfrage**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Antwort**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
