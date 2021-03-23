---
description: Ruft alle Benutzer in einem Array ab.
seo-description: Ruft alle Benutzer in einem Array ab.
seo-title: getAllUsers
solution: Experience Manager
title: getAllUsers
uuid: 7fe6ee2a-986d-464d-bc15-1e6444bcf13b
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 17%

---


# getAllUsers{#getallusers}

Ruft alle Benutzer in einem Array ab.

Syntax

## Autorisierte Benutzertypen {#section-68ed5f5fcc5348308dfe074c590caeaa}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-f092ca72f2024d66a1cec690aeab870a}

**Input (getAllUsersParam)**

<table id="table_1FE6DDADBD134E6D8BD4B52F1EAD2E85"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeInvalid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Auf: 
    <ul id="ul_FB9F59A8293B4CCA98E42EBF8412C77B"> 
     <li id="li_3C2E6C4D3478411FA1A34D5CBFFC8108"><span class="codeph"> ungültige Benutzer </span> tatsächlich einschließen. </li> 
     <li id="li_7FCA0DE4BE2248A690076FEC6854F5CE"><span class="codeph"> Benutzer </span> mit ungültigem Status werden nicht ausgelassen. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAllUsersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Ja | Array aller Benutzer. |
| `*`Codebegriff`*` | `Code Phrase` |  |  |

## Beispiele {#section-9c9a2d335513478da20652c1b1443731}

Dieses Codebeispiel gibt alle Benutzer zurück. Die Antwort wird wegen ihrer Kürze abgeschnitten.

**Anforderung**

```java
<ns1:getAllUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getAllUsersParam>
```

**Antwort**

```java
<ns1:getAllUsersReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userArray>
      <ns1:items>
         <ns1:userHandle>201|agentshadi@hotmail.com</ns1:userHandle>
         <ns1:firstName>333</ns1:firstName>
         <ns1:lastName>333</ns1:lastName>
         <ns1:email>my_email@someaddress.com</ns1:email>
         <ns1:role>TrialSiteUser</ns1:role>
         <ns1:isValid>true</ns1:isValid>
         <ns1:passwordExpires>2006-12-29T04:19:43.039Z</ns1:passwordExpires>
      </ns1:items>
   ...
   </ns1:userArray>
<ns1:getAllUsersReturn>
```

