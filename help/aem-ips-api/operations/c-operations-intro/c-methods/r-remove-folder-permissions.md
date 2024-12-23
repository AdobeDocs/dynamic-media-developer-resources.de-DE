---
title: removeFolderPermissions
description: Entfernt Ordnerberechtigungen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# removeFolderPermissions{#removefolderpermissions}

Entfernt Ordnerberechtigungen.

Syntax

## Autorisierte Benutzertypen {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-7efa68377fd846219b906d354ae64ed3}

**Input (removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Handle an das Unternehmen mit Ordnern mit Berechtigungen, die Sie entfernen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Verarbeiten Sie den Ordner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Wenn <span class="codeph"> wahr</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">Die Entfernung von Berechtigungen erfolgt über alle Vorgänge für Ordnerberechtigungen. </li> 
     </ul> </p> <p>Wenn „false<span class="codeph">: </span> 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">Der Vorgang betrifft nur den angegebenen Ordner. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (removeFolderPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-04390f0ec7cc460cb5d34d518e33e7a5}

Dieses Codebeispiel entfernt Berechtigungen aus einem Ordner und dessen Unterordnern. Legen Sie `updateChildren` auf `false` fest, um nur Berechtigungen aus dem übergeordneten Ordner zu entfernen.

**Anfrage**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Antwort**

Keine.
