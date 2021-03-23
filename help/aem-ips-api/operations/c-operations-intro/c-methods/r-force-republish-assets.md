---
description: Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um zu erzwingen, dass das Asset im nächsten Veröffentlichungsauftrag erneut veröffentlicht wird.
seo-description: Setzt den Veröffentlichungsstatus für ein oder mehrere Assets zurück, um zu erzwingen, dass das Asset im nächsten Veröffentlichungsauftrag erneut veröffentlicht wird.
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 7%

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

