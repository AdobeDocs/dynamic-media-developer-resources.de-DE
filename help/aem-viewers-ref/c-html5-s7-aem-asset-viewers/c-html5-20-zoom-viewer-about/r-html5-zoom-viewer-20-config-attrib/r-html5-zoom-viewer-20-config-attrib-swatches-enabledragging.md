---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic, Viewer, SDK/API, Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
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

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
