---
description: Gültige Werte für die Felder PropertySetType und createPropertySetTypeParam.
seo-description: Gültige Werte für die Felder PropertySetType und createPropertySetTypeParam.
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Scene7 Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PropertySetType{#propertysettype}

Gültige Werte für die Felder PropertySetType und createPropertySetTypeParam.

Die Werte umfassen:

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Geben Sie handle ein. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Firma Handle. <p>Hinweis:  Der Typ ist global, wenn der Firmen-Handle nicht vorhanden ist. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Geben Sie den Namen ein. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Einer der Eigenschaftssatztypen. Siehe Eingabe (<span class="codeph"> createPropertySetTypeParam</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Mehrere <span class="varname"> zulassen</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Gibt an, ob für diesen Typ mehrere Instanzen eines Eigenschaftensatzes an ein Objekt angehängt werden dürfen. </td> 
  </tr> 
 </tbody> 
</table>

