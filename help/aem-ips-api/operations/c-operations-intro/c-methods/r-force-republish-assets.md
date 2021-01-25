---
description: Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um zu erzwingen, dass das Asset im nächsten Veröffentlichungsauftrag erneut veröffentlicht wird.
seo-description: Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um zu erzwingen, dass das Asset im nächsten Veröffentlichungsauftrag erneut veröffentlicht wird.
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Dynamic Media Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 8%

---


# forceRepublishAssets{#forcerepublishassets}

Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um zu erzwingen, dass das Asset im nächsten Veröffentlichungsauftrag erneut veröffentlicht wird.

Syntax

## Autorisierte Benutzertypen {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**Input (forceRepublishAssetsParam)**

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
   <td colname="col4"> <p>Behandeln Sie die Firma mit den zurückzusetzenden Elementen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Gibt an, dass die Dateien für das Asset erneut auf den Versand-Servern veröffentlicht werden. Die Standardeinstellung ist <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Gibt an, dass die Katalogmetadaten, die für die Bereitstellung des Assets verwendet werden, synchronisiert werden, um sicherzustellen, dass sie aktuell sind. Dieser Parameter wird verwendet, um Racebedingungen zu lösen, die bei fast gleichzeitigen Aktualisierungen desselben Datensatzes auftreten können. Die Standardeinstellung ist <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Handles zu Assets, deren Veröffentlichungsstatus zurückgesetzt werden soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (forceRepublishAssetsParam)**

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
   <td colname="col2"> <span class="codeph"> Typen:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array von Aktualisierungen des Veröffentlichungsstatus. </p> </td> 
  </tr> 
 </tbody> 
</table>

