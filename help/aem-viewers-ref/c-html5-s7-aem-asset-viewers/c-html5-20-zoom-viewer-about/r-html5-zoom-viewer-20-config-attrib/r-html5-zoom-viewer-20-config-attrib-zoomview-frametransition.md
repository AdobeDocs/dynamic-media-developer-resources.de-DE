---
title: ZoomView.frameTransition
description: ZoomView.frameTransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
TQID: 'https://experienceleague.adobe.com/bnR4MQtKYsqMEDEyJN2iFpJNLMWcsc-s9mK4XQW5qpE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 4%

---

# ZoomView.frameTransition{#zoomview-frametransition}

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
