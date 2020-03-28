---
description: Fügt einem Array von Gruppen einen Benutzer hinzu.
seo-description: Fügt einem Array von Gruppen einen Benutzer hinzu.
seo-title: addGroupMembership
solution: Experience Manager
title: addGroupMembership
topic: Scene7 Image Production System API
uuid: a8e25f27-c300-424d-83ac-e41bb4cb7964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addGroupMembership{#addgroupmembership}

Fügt einem Array von Gruppen einen Benutzer hinzu.

Syntax

## Autorisierte Benutzertypen {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e250f6ddb13646808c6a8860b6442bc5}

**Input (addGroupMembershipParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Behandeln Sie den Benutzer, dessen Gruppenmitgliedschaft Sie hinzufügen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Handles zu den Gruppen, zu denen die Firma gehören soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addGroupMembershipParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-f7a1f40c3d7a40ea964b29056c734d81}

In diesem Beispiel wird einer Firma mit ` *`groupHandleArray`*`eine Gruppe hinzugefügt. In diesem Beispiel wird nur eine Gruppe verwendet.

**Anforderung**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Antwort**

Keine.
