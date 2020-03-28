---
description: 'Innerhalb dieses Typs ist das Feld "pageReset"für RenderSet- und Katalog-Bildelementtypen von Bedeutung '
seo-description: 'Innerhalb dieses Typs ist das Feld "pageReset"für RenderSet- und Katalog-Bildelementtypen von Bedeutung '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Scene7 Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

Innerhalb dieses Typs ist das Feld &quot;pageReset&quot;für RenderSet- und Katalog-Bild-Asset-Typen von Bedeutung:

* Zeigt beispielsweise `RenderSet`den Beginn einer neuen Render-Ansicht/Mustergruppe `pageReset` an.

* Bei &quot;Katalog&quot; `pageReset` wird der Beginn einer neuen Ansicht angezeigt. In der Regel gibt es pro Ansicht zwei Seitenbilder, aber Sie können mehr oder weniger haben.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset-Handle im Image-Set-Member-Array. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> pageReset <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Setzt die Seite zurück. <p>Die Einstellung wird ignoriert und der Wert wird für <span class="codeph"> ImageSet</span> und <span class="codeph"> Rotationsset</span>auf true festgelegt. </p></td> 
  </tr> 
 </tbody> 
</table>

