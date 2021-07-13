---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
feature: Dynamic Media Classic,Viewer,SDK/API,Inline-Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade  </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ an, den der Effekt angewendet wird, wenn die Flyout-Ansicht ein- oder ausgeblendet wird. Bei <span class="codeph"> none </span> wird das Flyout-Bild sofort angezeigt, wenn es aktiviert und fertig ist. <span class="codeph"> Folie </span> sorgt dafür, dass die Animation der Folie von links nach rechts abgespielt wird; <span class="codeph"> Fade </span> wendet eine Alphakanäle auf das Flyout-Bild an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der Animation der Sendung dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation der Sendung initiiert, und dem Beginn der Animation der Sendung selbst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der ausgeblendeten Animation benötigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation zum Ausblenden auslöst, und dem Beginn der Animation zum Ausblenden selbst. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
