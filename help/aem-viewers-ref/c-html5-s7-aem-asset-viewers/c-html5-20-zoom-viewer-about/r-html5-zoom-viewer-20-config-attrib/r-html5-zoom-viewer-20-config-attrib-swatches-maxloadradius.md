---
title: Swatches.maxLoadRadius
description: Swatches.maxLoadRadius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
TQID: 'https://experienceleague.adobe.com/lx-kygwnrE26h0YA1tPfv59apt-uJMYSh2shtavHo-Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 5%

---

# Swatches.maxLoadRadius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadNbr</span></span> </p> </td> 
   <td> <p>Gibt das Verhalten beim Vorausfüllen der Komponente an. Wenn auf <span class="codeph"> -1 festgelegt</span> werden alle Farbfelder gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Wenn auf <span class="codeph"> 0 festgelegt</span> werden nur sichtbare Farbfelder geladen. </p> <p><span class="codeph"><span class="varname"> preloadNbr</span></span> legt fest, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`

