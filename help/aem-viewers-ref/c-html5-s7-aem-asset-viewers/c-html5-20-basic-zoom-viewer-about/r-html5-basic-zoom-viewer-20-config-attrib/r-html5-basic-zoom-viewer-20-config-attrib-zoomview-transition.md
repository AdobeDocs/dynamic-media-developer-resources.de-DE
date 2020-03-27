---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.Transition
solution: Experience Manager
title: ZoomView.Transition
topic: Dynamic media
uuid: f579397b-a449-42fe-b0a7-f0da65a6a248
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.Transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`Zeitbeschleunigung`*[, *``*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Zeit</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für eine einzelne Zoomschritt-Aktion dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Lockerung</span></span> </p> </td> 
   <td colname="col2"> <p> Erstellt eine Illusion der Beschleunigung oder Verzögerung, die die Transition natürlicher erscheinen lässt. Sie können die Lockerung auf einen der folgenden einstellen: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linear) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratisch) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (kubisch) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (Quartil) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (Chinesisch) </li> 
     </ul> </p> <p>Der automatische Modus verwendet immer eine lineare Transition, wenn der elastische Zoom deaktiviert ist (Standard). Andernfalls passt es zu einer der anderen Beschleunigungsfunktionen, die auf der Transition basieren. Das heißt, je kürzer die Transition ist, desto höher wird die Beschleunigungsfunktion verwendet, um den Beschleunigungs- oder Verzögerungseffekt zu beschleunigen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
