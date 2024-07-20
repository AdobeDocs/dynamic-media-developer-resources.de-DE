---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`hidetime`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ an, den der Effekt angewendet wird, wenn die Flyout-Ansicht ein- oder ausgeblendet wird. Bei <span class="codeph"> none </span> erscheint das Flyout-Bild sofort, wenn es aktiviert und fertig ist. <span class="codeph"> Folie </span> sorgt dafür, dass die Dia-Animation von links nach rechts abgespielt wird; <span class="codeph"> Fade </span> wendet eine Alpha-Transition auf das Flyout-Bild an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der Animation der Sendung dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation der Sendung initiiert, und dem Beginn der Animation der Sendung selbst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span> </span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der ausgeblendeten Animation benötigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation zum Ausblenden auslöst, und dem Beginn der Animation zum Ausblenden selbst. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
