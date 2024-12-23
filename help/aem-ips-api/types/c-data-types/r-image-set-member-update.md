---
description: Innerhalb dieses Typs ist das Feld „pageReset“ für die Asset-Typen „renderSet“ und „Catalog image“ aussagekräftig
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

Innerhalb dieses Typs ist das Feld „pageReset“ für die Asset-Typen „renderSet“ und „Catalog image“ aussagekräftig:

* `pageReset` gibt `RenderSet` den Beginn einer neuen Render-Ansicht/Farbfeldgruppe an.

* Für den Katalog gibt `pageReset` den Beginn einer neuen Seitenansicht an. In der Regel gibt es zwei Seitenbilder pro Seitenansicht, es können aber auch mehr oder weniger vorhanden sein.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> AssetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset-Handler im Bildset-Member-Array. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Setzt die Seite zurück <p>Die Einstellung wird ignoriert, und der Wert wird für <span class="codeph"> ImageSet</span> und <span class="codeph"> SpinSet</span> auf „true“ erzwungen. </p></td> 
  </tr> 
 </tbody> 
</table>
