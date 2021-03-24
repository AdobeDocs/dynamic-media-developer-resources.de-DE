---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Viewer,SDK/API,Mix-Mediensets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Aktiviert bzw. deaktiviert die Möglichkeit, dass ein Benutzer die Muster mit einer Maus oder mit Berührungsgesten durchblättert </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funktionen im Bereich <span class="codeph"> 0-1 </span>. Es handelt sich um einen <span class="codeph"> % </span>-Wert für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn sie auf <span class="codeph"> 1 </span> eingestellt ist, wird sie mit der Maus verschoben. Wenn sie auf <span class="codeph"> 0 </span> eingestellt ist, können Sie sich nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
