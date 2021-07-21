---
description: Gibt Informationen zum angegebenen Unternehmen zurück, einschließlich des Unternehmens-Handles, des Unternehmensnamens, des Stammpfads und des Ablaufdatums. Sie müssen entweder companyHandle oder companyName angeben, deren Informationen Sie abrufen möchten.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72bd223b-c99a-48a3-9c0a-d1af392d904c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 8%

---

# getCompanyInfo{#getcompanyinfo}

Gibt Informationen zum angegebenen Unternehmen zurück, einschließlich des Unternehmens-Handles, des Unternehmensnamens, des Stammpfads und des Ablaufdatums. Sie müssen entweder companyHandle oder companyName angeben, deren Informationen Sie abrufen möchten.

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

**Eingabe (getCompanyInfoParam)**

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Es ist entweder <span class="codeph"> <span class="varname"> companyHandle</span> </span> oder <span class="codeph"> <span class="varname"> companyName</span> </span> erforderlich. </p> </td> 
   <td colname="col4"> <p>Der Handle des Unternehmens, dessen Informationen Sie abrufen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Es ist entweder <span class="codeph"> <span class="varname"> companyHandle</span> </span> oder <span class="codeph"> <span class="varname"> companyName</span> </span> erforderlich. </p> </td> 
   <td colname="col4"> <p>Der Name des Unternehmens, dessen Informationen Sie abrufen möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (getCompanyInfoReturn)**

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:Firma</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handhabung und andere beschreibende Informationen über das Unternehmen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Dieses Codebeispiel gibt alle Informationen über ein Unternehmen mithilfe eines Unternehmensnamens und -handle zurück. Es werden Daten zurückgegeben, die der Antwort ähneln, die beim Erstellen eines Unternehmens empfangen wurde.

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
