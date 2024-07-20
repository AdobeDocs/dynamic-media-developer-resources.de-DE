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
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>Gibt den Typ des Effekts an, der auf die Bildänderung angewendet wird. Das Attribut <span class="codeph"> none </span> steht für keine Transition; die Rahmenänderung erfolgt sofort. Das Attribut <span class="codeph"> fade </span> bedeutet eine Überblendung zwischen alten und neuen Frames. Das Attribut <span class="codeph"> slide </span> aktiviert die Transition, bei der der alte Frame aus der Ansicht herausrutscht und der neue Frame eingeschaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer </span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer (in Sekunden) des Übergangseffekts <span class="codeph"> Überblendung </span> oder <span class="codeph"> Folie </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Abstand </span> </span> </p> </td> 
   <td colname="col2"> <p>Der Abstand zwischen benachbarten Frames in der Transition <span class="codeph"> Folie </span> hat den Bereich von <span class="codeph"> 0 </span> bis <span class="codeph"> 1 </span> und ist relativ zur Breite der Komponente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

Keine.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
