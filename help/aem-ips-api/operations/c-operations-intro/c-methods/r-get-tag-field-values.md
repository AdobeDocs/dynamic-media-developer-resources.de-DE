---
description: Ruft alle Tag-Wörterbuchwerte ab, die für ein oder mehrere Tag-Felder definiert sind.
seo-description: Ruft alle Tag-Wörterbuchwerte ab, die für ein oder mehrere Tag-Felder definiert sind.
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
topic: Dynamic Media Image Production System API
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, die das Tag-Feld enthält. |
| `*`fieldHandleArray`*` | `types:HandleArray` | Ja | Ein Array von field-Handles für Tag-Werte, die zurückgegeben werden sollen. |

**Output (getTagFieldValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | Ja | Ein Array der Tag-Werte im Wörterbuch für jedes angeforderte Feld. |

## Beispiele {#section-4492742614e44bb191a7d397dc1a1407}

**Anforderung**

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

