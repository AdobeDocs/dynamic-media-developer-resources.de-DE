---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showTime`*[, *`showDelay`*[, *`hideTime`*[, *`hideDelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des Effekts an, der beim Ein- oder Ausblenden der Flyout-Ansicht angewendet wird. Mit <span class="codeph"> </span> wird das Flyout-Bild sofort angezeigt, wenn es aktiviert und bereit ist. <span class="codeph"> </span> Folienanimation wird von der Folie in die Richtung von links nach rechts abgespielt. <span class="codeph"> Überblendung </span> wendet einen Alpha-Übergang auf das Flyout-Bild an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die die Animation in der Sendung dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showDelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen Benutzeraktion, die die Animation der Sendung initiiert, und dem Beginn der Animation der Sendung selbst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hideTime </span> </span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die die Animation zum Ausblenden dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hideDelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation zum Ausblenden initiiert, und dem Beginn der Animation zum Ausblenden selbst. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
