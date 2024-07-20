---
description: Ruft einen Eigenschaftssatztyp mithilfe eines Handles für ein Unternehmen und den Namen des Eigenschaftssatztyps ab. Ruft eine Typstruktur mit dem Handle zum Typ sowie den Eigenschaftstyp ab.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 9%

---

# getPropertySetType{#getpropertysettype}

Ruft einen Eigenschaftssatztyp mithilfe eines Handles für ein Unternehmen und den Namen des Eigenschaftssatztyps ab. Ruft eine Typstruktur mit dem Handle zum Typ sowie den Eigenschaftstyp ab.

Syntax

## Autorisierte Benutzertypen {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-c9a53400c44744668bd7915f72d2bf3d}

**Input (getPropertySetTypeParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Nein | Der Handle für das Unternehmen. Optional, da ein Eigenschaftssatz-Typ mehreren Unternehmen angehören kann. |
| name | `xsd:string` | Ja | Name des Eigenschaftssatztyps. |

**Output (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Die Typstruktur, die Folgendes enthält: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Handle. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Geben Sie den Namen ein. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Eigenschaftstyp. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Wert, der angibt, ob der Typ mehrere Eigenschaftstypen zulässt. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-1b57199415e34a8fa449f864f8895b14}

Dieses Codebeispiel gibt einen Eigenschaftssatztyp nach Name zurück.

**Anfrage**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Antwort**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```
