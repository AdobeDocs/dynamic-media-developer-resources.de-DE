---
description: Definiert Suchbedingungen für Tag-Felder.
seo-description: Definiert Suchbedingungen für Tag-Felder.
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
topic: Scene7 Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# TagCondition{#tagcondition}

Definiert Suchbedingungen für Tag-Felder.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Tag-Feldgriff. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Hängt vom Tag-Feldtyp und davon ab, ob das Feld value oder valueArray verwendet wird. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Wenn <span class="codeph"> value</span> übergeben wird, muss <span class="codeph"> op</span> die String-Konstante stimmt überein. Die Bedingung stimmt mit allen Elementen überein, die mit dem Tag-Wert verknüpft sind. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Wenn <span class="codeph"> valueArray</span> übergeben wird, kann das Feld op die Konstante <span class="codeph"> MatchesAny</span> für einzelne oder mehrwertige Tag-Felder sein. Eine <span class="codeph">-Bedingung stimmt mit Beliebiger</span>-Bedingung überein mit jedem Element, das mit mindestens einem der Tag-Werte in <span class="codeph"> valueArray</span> verknüpft ist. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Bei Feldern mit mehreren Werten kann das Feld "op"auf die Konstante <span class="codeph"> MatchesAll</span> mit dem Feld <span class="codeph"> valueArray</span> eingestellt werden. In diesem Fall stimmt die Bedingung nur mit Elementen überein, die mit allen Tag-Werten in <span class="codeph"> valueArray</span> (möglicherweise zusätzlich zu anderen Tag-Werten) verknüpft sind. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ein übereinstimmender Wert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Mehrere übereinstimmende Werte. </td> 
  </tr> 
 </tbody> 
</table>

