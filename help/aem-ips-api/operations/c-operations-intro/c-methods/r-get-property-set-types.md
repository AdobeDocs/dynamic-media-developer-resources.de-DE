---
description: Ruft die Eigenschaftssatztypen ab, die mit dem angegebenen Unternehmen verknüpft sind, bzw. globale Eigenschaftssatztypen, wenn kein Unternehmen angegeben ist.
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 12%

---

# getPropertySetTypes{#getpropertysettypes}

Ruft die Eigenschaftssatztypen ab, die mit dem angegebenen Unternehmen verknüpft sind, bzw. globale Eigenschaftssatztypen, wenn kein Unternehmen angegeben ist.

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

**Eingabe (getPropertySetTypesParam)**

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
   <td colname="col4">Der Handle für das Unternehmen, mit dem die Eigenschaftssatztypen verknüpft sind. <p>Lassen Sie die Rückgabe globaler Eigenschaftssatztypen aus. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (getPropertySetTypesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Ja | Ein Array von Eigenschaftssatztypen, die mit dem angegebenen Unternehmen verknüpft sind, oder die globalen Eigenschaftssatztypen, wenn kein Unternehmen angegeben wurde. |

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
