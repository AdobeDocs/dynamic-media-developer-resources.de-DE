---
description: Entfernt Ordnerberechtigungen.
solution: Experience Manager
title: removeFolderPermissions
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

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
   <td colname="col4"> Der Griff zur Firma mit Ordnern, die Sie entfernen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Behandeln Sie den Ordner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Wenn <span class="codeph"> true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">Das Entfernen von Berechtigungen wird durch alle Vorgänge mit Ordnerberechtigungen übertragen. </li> 
     </ul> </p> <p>Wenn <span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">Der Vorgang betrifft nur den angegebenen Ordner. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (removeFolderPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-04390f0ec7cc460cb5d34d518e33e7a5}

In diesem Codebeispiel werden Berechtigungen aus einem Ordner und seinen Unterordnern entfernt. Setzen Sie `updateChildren` auf `false`, wenn Sie nur Berechtigungen aus dem übergeordneten Ordner entfernen müssen.

**Anforderung**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Antwort**

Keine.
