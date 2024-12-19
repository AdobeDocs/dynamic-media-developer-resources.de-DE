---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
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

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
