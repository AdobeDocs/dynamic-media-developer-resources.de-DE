---
description: Fügt dem System eine Firma hinzu.
seo-description: Fügt dem System eine Firma hinzu.
seo-title: addCompany
solution: Experience Manager
title: addCompany
topic: Scene7 Image Production System API
uuid: 2f00a06d-40d1-4ba3-a317-6ea91e25beb3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# addCompany{#addcompany}

Fügt dem System eine Firma hinzu.

Sendet den Namen der Firma, die dem System hinzugefügt werden soll, und sendet optional, ob die Firma abläuft.

Wenn dieser Vorgang aufgerufen wird, erhält das System den Typ ` *`companyInfo`*`, der einen Firmen-Handle und beschreibende Felder enthält. Wenn der angeforderte Firmen-Name bereits im System vorhanden ist, wird ein `ipsApiFault` ausgegeben.

## Autorisierte Benutzertypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-c64a21b72585447880760db9e7a12ccb}

**Input (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Name der hinzuzufügenden Firma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> expires</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das Ablaufdatum der Firma. Geben Sie die Zeitzone mit der Anforderung für dieses Feld ein. Die Zeitzonen werden auf "Central Time"eingestellt. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handhabung und Name, Stammpfad, Ablaufdatum und Uhrzeit der neuen Firma. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-4c8f1bb40d154c77a7b410468206e52b}

Dieses Beispiel zeigt eine Anforderung zum Hinzufügen einer Firma zum IPS-System und die Antwort mit detaillierten Informationen zur hinzugefügten Firma, die zum Durchführen anderer Vorgänge erforderlich ist.

**Anforderung**

```java
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Antwort**

```java
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```

