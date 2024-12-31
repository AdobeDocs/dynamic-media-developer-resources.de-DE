---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duration`*[, *`spacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|</span> </p> </td> 
   <td colname="col2"> <p>Gibt den Typ des Effekts an, der auf die Rahmenänderung angewendet wird. Das Attribut <span class="codeph">none“ </span> für „no transition“. Die Frame-Änderung erfolgt sofort. Das Attribut <span class="codeph"> fade bedeutet </span> eine Überblendung zwischen alten und neuen Frames. Das Attribut <span class="codeph"> Folie aktiviert </span> Transition, in der der alte Rahmen aus der Ansicht verschoben und der neue Rahmen eingeschoben wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer </span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer (in Sekunden) <span class="codeph"> Überblendungs-</span> oder <span class="codeph"> Folienübergangseffekts </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Abstand </span> </span> </p> </td> 
   <td colname="col2"> <p>Der Abstand zwischen benachbarten Rahmen in <span class="codeph"> </span>, hat den Bereich von <span class="codeph"> 0 </span> bis <span class="codeph"> 1 </span> und ist relativ zur Bauteilbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

Keine.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
