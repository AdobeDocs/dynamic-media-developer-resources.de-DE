---
title: CarouselView.frameTransition
description: CarouselView.frameTransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
TQID: 'https://experienceleague.adobe.com/65cLC5DOqdGrbVpMMy6gLBNL4F3WRqipNqIlpBIK-GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 4%

---

# CarouselView.frameTransition{#carouselview-frametransition}

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
