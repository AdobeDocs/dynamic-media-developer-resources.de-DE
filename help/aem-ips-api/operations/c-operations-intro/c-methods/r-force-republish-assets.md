---
description: Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um die erneute Veröffentlichung des Assets im nächsten Veröffentlichungsauftrag zu erzwingen.
solution: Experience Manager
title: forceRepublishAssets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4c75af38-4791-4f21-8d1b-4855fcdfd4b1
TQID: 'https://experienceleague.adobe.com/G7A1o0gfERLSCW6xzt9sx2wwXNyQeJ8s9-DcCQyIWGM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 9%

---

# forceRepublishAssets{#forcerepublishassets}

Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um die erneute Veröffentlichung des Assets im nächsten Veröffentlichungsauftrag zu erzwingen.

Syntax

## Autorisierte Benutzertypen {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**Eingabe (forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Verarbeiten Sie das Unternehmen mit den Assets, die zurückgesetzt werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Gibt an, dass die Dateien für das Asset erneut auf den Bereitstellungs-Servern veröffentlicht werden. Die Standardeinstellung ist <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Gibt an, dass die Katalogmetadaten, die für die Bereitstellung des Assets verwendet werden, synchronisiert werden, um sicherzustellen, dass es aktuell ist. Dieser Parameter wird verwendet, um Racebedingungen zu beheben, die bei nahezu gleichzeitigen Aktualisierungen desselben Datensatzes auftreten können. Die Standardeinstellung ist <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Handles für Assets, deren Veröffentlichungsstatus zurückgesetzt werden soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Aktualisierungen des Veröffentlichungsstatus. </p> </td> 
  </tr> 
 </tbody> 
</table>

