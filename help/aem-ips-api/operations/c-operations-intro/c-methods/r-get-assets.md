---
title: getAssets
description: Gibt Assets aus dem Image Production System (IPS) zurück.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 3b63da9c-f10a-40bf-8e3c-4f0bfc53d74c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 14%

---

# getAssets{#getassets}

Gibt Assets aus dem Image Production System (IPS) zurück.

Syntax

## Autorisierte Benutzertypen {#section-4673c1c9f4314160af8b165eb2dd20cc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Gibt nur die Assets zurück, auf die der Benutzer Zugriff hat.

## Parameter {#section-bb9cf1ab19ea47acbd9ae58646dbe273}

**Eingabe (getAssetsParam)**

<table id="table_15CDEFC7F836411C80AA122E3A701C77"> 
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
   <td colname="col4"> <p>Das Handle des Unternehmens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Identität eines bestimmten Benutzers annehmen. Wird nur von Administratoren verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Filtern nach Gruppe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Stammordner zum Abrufen von Ordnern und allen Unterordnern auf Blattebene. Wenn diese Option ausgeschlossen ist, wird der Stammordner des Unternehmens verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>In der Antwort enthaltene Felder und Unterfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:StringArray</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Felder und Unterfelder, die aus der Antwort ausgeschlossen sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (getAssetsReturn)**

<table id="table_694932BBBD2C4167871380B2CF514BEA"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:AssetArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, die den Filterkriterien entsprechen. </p> </td> 
  </tr> 
 </tbody> 
</table>
