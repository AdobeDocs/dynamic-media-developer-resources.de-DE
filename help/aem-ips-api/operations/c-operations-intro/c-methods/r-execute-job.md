---
description: Führt einen bestimmten Auftrag aus.
seo-description: Führt einen bestimmten Auftrag aus.
seo-title: executeJob
solution: Experience Manager
title: executeJob
topic: Dynamic Media Image Production System API
uuid: e73223c1-9032-4745-92b6-a5840949a824
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---


# executeJob{#executejob}

Führt einen bestimmten Auftrag aus.

Syntax

## Autorisierte Benutzertypen {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Input (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Griff der Firma, zu der der Auftrag gehört. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Griff zum auszuführenden Auftrag. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (executeJobReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-96f71aa58a954293b9a98ff96d86f232}

In diesem Codebeispiel wird ein Auftrag ausgeführt, der in IPS ausgeführt werden soll.

**Anforderung**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**Antwort**

Keine.
