---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`durationabstand`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>Gibt den Typ des Effekts an, der bei einer Bildänderung angewendet wird. <span class="codeph"> keiner  </span> steht für keine Transition; Rahmenänderungen werden sofort vorgenommen. <span class="codeph"> "Überblenden" </span> bedeutet eine Überblendung zwischen alten und neuen Frames. <span class="codeph"> Dia  </span> aktiviert die Transition, bei der der alte Rahmen aus der Ansicht verschoben wird und der neue Rahmen hineingegleitet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer  </span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer (in Sekunden) des Effekts <span class="codeph"> Überblendung </span> oder <span class="codeph"> Transition </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Abstand  </span> </span> </p> </td> 
   <td colname="col2"> <p>Der Abstand zwischen benachbarten Frames in der <span class="codeph">-Transition </span> hat den Bereich zwischen <span class="codeph"> 0 </span> und <span class="codeph"> 1 </span> und ist relativ zur Komponentenbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

Keine.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
