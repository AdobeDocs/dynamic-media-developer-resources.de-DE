---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
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
