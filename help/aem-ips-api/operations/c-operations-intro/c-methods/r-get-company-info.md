---
description: Gibt Informationen zur angegebenen Firma zurück, einschließlich des Firma-Handles, des Namens der Firma, des Stammpfads und des Ablaufdatums. Sie müssen entweder companyHandle oder companyName angeben, deren Informationen Sie abrufen möchten.
seo-description: Gibt Informationen zur angegebenen Firma zurück, einschließlich des Firma-Handles, des Namens der Firma, des Stammpfads und des Ablaufdatums. Sie müssen entweder companyHandle oder companyName angeben, deren Informationen Sie abrufen möchten.
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
topic: Scene7 Image Production System API
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanyInfo{#getcompanyinfo}

Gibt Informationen zur angegebenen Firma zurück, einschließlich des Firma-Handles, des Namens der Firma, des Stammpfads und des Ablaufdatums. Sie müssen entweder companyHandle oder companyName angeben, deren Informationen Sie abrufen möchten.

Syntax

## Autorisierte Benutzertypen {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-7dec8871c89a414c9f066adade1831d8}

**Input (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Es ist entweder <span class="codeph"> das UnternehmenHandle <span class="varname"></span> oder </span> der <span class="codeph"> Unternehmensname <span class="varname"> erforderlich</span> </span> . </p> </td> 
   <td colname="col4"> <p>Der Griff der Firma, deren Informationen Sie abrufen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Firmenname</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Es ist entweder <span class="codeph"> das UnternehmenHandle <span class="varname"></span> oder </span> der <span class="codeph"> Unternehmensname <span class="varname"> erforderlich</span> </span> . </p> </td> 
   <td colname="col4"> <p>Der Name der Firma, deren Informationen Sie abrufen möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:Firma</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handhabung und andere beschreibende Informationen zur Firma. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Dieses Codebeispiel gibt alle Informationen über eine Firma unter Verwendung eines Firma-Namens und -Handles zurück. Gibt Daten zurück, die der beim Erstellen einer Firma erhaltenen Antwort ähnlich sind.

**Anforderung**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Antwort**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

