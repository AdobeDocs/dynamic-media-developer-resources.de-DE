---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`duration`*[, *`spacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|</span> </p> </td> 
   <td colname="col2"> <p>Gibt den Typ des Effekts an, der auf die Rahmenänderung angewendet wird. Beispiel: <span class="codeph"> Keine </span> steht für „Kein Übergang“. Frame-Änderungen werden sofort vorgenommen. und </p> <p> <span class="codeph"> Überblendung bedeutet </span> Überblendung zwischen alten und neuen Bildern. Schließlich </p> <p> <span class="codeph"> Dia-</span> aktiviert die Überblendung, in der der alte Rahmen aus der Ansicht verschoben wird, und der neue Rahmen in die Ansicht verschoben wird. </p> </td> 
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

`frametransition=fade,0.3`
