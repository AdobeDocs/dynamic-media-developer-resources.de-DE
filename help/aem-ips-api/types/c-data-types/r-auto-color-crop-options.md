---
description: Optionen zum automatischen Beschneiden von Bildern basierend auf Farbe.
solution: Experience Manager
title: AutoColorCropOptions
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 9%

---


# AutoColorCropOptions{#autocolorcropoptions}

Optionen zum automatischen Beschneiden von Bildern basierend auf Farbe.

Syntax

## Parameter {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auswahl der AutoCrop-Ecke. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Toleranz</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Dublette</span> </td> 
   <td colname="col3">Farbübereinstimmungsspezifikation. Verwendet: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0, um Farben exakt abzugleichen. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1, um die meisten Farbunterschiede zu aktivieren. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

