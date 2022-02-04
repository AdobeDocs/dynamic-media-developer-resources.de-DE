---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Aktiviert oder deaktiviert die Möglichkeit für einen Benutzer, mit der Maus oder durch Berührungsgesten zu scrollen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funktionen innerhalb der <span class="codeph"> 0-1 </span> Bereich. Es ist ein <span class="codeph"> % </span> Wert für Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn sie auf <span class="codeph"> 1 </span>, bewegt er sich mit der Maus. Wenn sie auf <span class="codeph"> 0 </span>, können Sie sich nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
