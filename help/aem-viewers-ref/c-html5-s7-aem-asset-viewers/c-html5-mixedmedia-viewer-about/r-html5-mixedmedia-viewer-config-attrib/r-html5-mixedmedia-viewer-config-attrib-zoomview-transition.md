---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bb00a1c9-aa6f-428f-8d57-241ee1efa082
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`time`*[, *`leasing`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für die Aktion eines einzelnen Zoomschritts benötigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> leasing</span></span> </p> </td> 
   <td colname="col2"> <p> Erstellt eine Illusion der Beschleunigung oder Verzögerung, die den Übergang natürlicher erscheinen lässt. Sie können die Lockerung auf eine der folgenden Optionen einstellen: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linear) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratisch) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (kubisch) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (Quartil) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintisch) </li> 
     </ul> </p> <p>Der Auto-Modus verwendet immer einen linearen Übergang, wenn der elastische Zoom deaktiviert ist (Standard). Andernfalls passt es auf Grundlage der Übergangszeit zu einer der anderen Erleichterungsfunktionen. Das heißt, je kürzer die Übergangszeit ist, desto höher wird die Lockerungsfunktion verwendet, um die Beschleunigung oder Verzögerung zu beschleunigen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
