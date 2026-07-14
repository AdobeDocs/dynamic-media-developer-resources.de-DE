---
title: ZoomView.iconEffect
description: ZoomView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
TQID: 'https://experienceleague.adobe.com/kkASM0uYyw3UqHWf-AVpztZvnpWg4t7djmqVkFWAxR4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# ZoomView.iconEffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert den <span class="codeph"> iconeffect</span>, der über dem Bild angezeigt wird, wenn das Bild zurückgesetzt wird und eine Aktion angezeigt werden kann, die mit dem Bild interagiert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Anzahl</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft der <span class="codeph"> IconEffect</span> maximal angezeigt werden kann. Der Wert <span class="codeph"> -1</span> bedeutet, dass das Symbol immer unbegrenzt wieder angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verblasst</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Einblenden- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> automatisch ausblenden</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, die der <span class="codeph"> iconeffect</span> vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach Abschluss der Einblendanimation, aber vor Beginn der Ausblendanimation. Bei einer Einstellung von <span class="codeph"> 0</span> wird das Verhalten zum automatischen Ausblenden deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

