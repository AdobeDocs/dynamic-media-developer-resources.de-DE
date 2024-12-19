---
description: Optionen zum automatischen Zuschneiden von Bildern basierend auf Transparenz.
solution: Experience Manager
title: AutoTransparentCropOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 10%

---

# [!DNL AutoTransparentCropOptions]{#autotransparentcropoptions}

Optionen zum automatischen Zuschneiden von Bildern basierend auf Transparenz.

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
   <td colname="col1"> <span class="codeph"> Toleranz</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Entfernt Leerraum von Bildkanten basierend auf Transparenz. Verwendet: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0, um Farben genau zuzuordnen. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1, um die meisten Farbunterschiede zu aktivieren. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
