---
description: Definiert Suchbedingungen für Tag-Felder.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# [!DNL TagCondition]{#tagcondition}

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
   <td colname="col3"> Tag-Feld-Handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Hängt vom Tag-Feldtyp ab und davon, ob das Feld value oder valueArray verwendet wird. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Wenn <span class="codeph"> value</span> übergeben wird, <span class="codeph"> op</span> muss die Zeichenfolgenkonstante Übereinstimmung sein. Die Bedingung stimmt mit jedem Asset überein, das mit dem Tag-Wert verknüpft ist. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Wenn <span class="codeph"> valueArray</span> übergeben wird, kann das Feld "op"die Konstante sein. <span class="codeph"> MatchesAny</span> für einzelne oder mehrwertige Tag-Felder. A <span class="codeph"> MatchesAny</span> -Bedingung stimmt mit jedem Asset überein, das mit mindestens einem der Tag-Werte in <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Bei Tagfeldern mit mehreren Werten kann das Feld op auf die Konstante eingestellt werden <span class="codeph"> MatchesAll</span> mit dem <span class="codeph"> valueArray</span> -Feld. In diesem Fall stimmt die Bedingung nur mit Assets überein, die mit allen Tag-Werten in <span class="codeph"> valueArray</span> (möglicherweise zusätzlich zu anderen Tag-Werten). </li>
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
