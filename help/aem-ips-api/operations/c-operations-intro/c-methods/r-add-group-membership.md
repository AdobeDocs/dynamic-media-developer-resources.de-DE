---
description: Fügt einen Benutzer zu einem Array von Gruppen hinzu.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 12%

---

# addGroupMembership{#addgroupmembership}

Fügt einen Benutzer zu einem Array von Gruppen hinzu.

Syntax

## Autorisierte Benutzertypen {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e250f6ddb13646808c6a8860b6442bc5}

**Eingabe (addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Behandeln Sie den Benutzer, dessen Gruppenmitgliedschaft Sie hinzufügen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Handles zu den Gruppen, denen das Unternehmen angehören soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (addGroupMembershipParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-f7a1f40c3d7a40ea964b29056c734d81}

In diesem Beispiel wird einem Unternehmen mit groupHandleArray eine Gruppe hinzugefügt. In diesem Beispiel wird nur eine Gruppe verwendet.

**Anforderung**

```java {.line-numbers}
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Antwort**

Keine.
