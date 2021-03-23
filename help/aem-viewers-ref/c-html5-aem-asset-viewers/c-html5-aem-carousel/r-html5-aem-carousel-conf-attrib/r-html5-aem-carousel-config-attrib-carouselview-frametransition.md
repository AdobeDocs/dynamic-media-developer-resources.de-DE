---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`durationabstand`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>Gibt den Typ des Effekts an, der bei einer Bildänderung angewendet wird. <span class="codeph"> keiner  </span> steht für keine Transition; Frame-Änderung wird sofort ausgeführt. </p> <p> <span class="codeph"> "Überblenden" </span> bedeutet eine Überblendung zwischen alten und neuen Frames. </p> <p> <span class="codeph"> Dia  </span> aktiviert die Transition, bei der der alte Rahmen aus der Ansicht verschoben wird und der neue Rahmen hineingegleitet wird. </p> </td> 
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

`frametransition=fade,0.3`
