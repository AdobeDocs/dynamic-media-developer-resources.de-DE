---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic,Viewer,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`durationspacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>Gibt den Typ des Effekts an, der auf die Bildänderung angewendet wird. <span class="codeph"> Keine  </span> steht für keine Transition; Frame-Änderung erfolgt sofort. <span class="codeph"> Überblendung  </span> bedeutet einen verblassten Übergang zwischen alten und neuen Frames. <span class="codeph"> Folie  </span> aktiviert Transition, bei der der alte Rahmen aus der Ansicht herausrutscht und der neue Rahmen eingeschaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer (in Sekunden) des Übergangseffekts <span class="codeph"> Überblendung </span> oder <span class="codeph"> Folie </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spacing  </span> </span> </p> </td> 
   <td colname="col2"> <p>Der Abstand zwischen benachbarten Frames in der <span class="codeph"> Folie </span> hat den Bereich zwischen <span class="codeph"> 0 </span> und <span class="codeph"> 1 </span> und ist relativ zur Breite der Komponente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

Keine.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
