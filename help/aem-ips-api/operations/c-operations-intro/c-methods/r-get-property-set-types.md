---
description: Ruft die mit der angegebenen Firma verknüpften Eigenschaftssatztypen oder globale Eigenschaftssatztypen ab, wenn keine Firma angegeben ist.
seo-description: Ruft die mit der angegebenen Firma verknüpften Eigenschaftssatztypen oder globale Eigenschaftssatztypen ab, wenn keine Firma angegeben ist.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Scene7 Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 11%

---


# getPropertySetTypes{#getpropertysettypes}

Ruft die mit der angegebenen Firma verknüpften Eigenschaftssatztypen oder globale Eigenschaftssatztypen ab, wenn keine Firma angegeben ist.

Syntax

## Autorisierte Benutzertypen {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Input (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Erforderlich </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Das Handle für die Firma, mit der die Eigenschaftssatztypen verknüpft sind. <p>Lassen Sie diese Option deaktiviert, wenn Sie globale Eigenschaftssatztypen zurückgeben möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getPropertySetTypesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`typeArray`*` | `types:PropertySetTypeArray` | Ja | Ein Array von Eigenschaftssatztypen, die mit der angegebenen Firma verknüpft sind, oder, falls keine Firma angegeben wurde, mit den Typen des globalen Eigenschaftensatzes. |

## Beispiele {#section-280c406a90864409856aee44d4069a52}

**Anforderung**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Antwort**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

