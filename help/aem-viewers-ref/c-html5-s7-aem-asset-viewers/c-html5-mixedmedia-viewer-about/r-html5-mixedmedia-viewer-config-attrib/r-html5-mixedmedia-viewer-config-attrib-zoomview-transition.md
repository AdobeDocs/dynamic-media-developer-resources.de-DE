---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bb00a1c9-aa6f-428f-8d57-241ee1efa082
TQID: 'https://experienceleague.adobe.com/k7wLDH-nUWtlCQN-AD3-HRLMDgZSthC1kwWPTh2LHHM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`time`*[, *`easing`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zeit</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für einen einzelnen Zoom-Schritt ausführen soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Erleichterung</span></span> </p> </td> 
   <td colname="col2"> <p> Erstellt eine Illusion von Beschleunigung oder Verzögerung, die den Übergang natürlicher erscheinen lässt. Sie können die Lockerung auf eine der folgenden Optionen einstellen: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automatisch) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linear) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratisch) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (kubisch) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartisch) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (Chintisch) </li> 
     </ul> </p> <p>Der Auto-Modus verwendet immer einen linearen Übergang, wenn das elastische Zoomen deaktiviert ist (Standard). Andernfalls passt es zu einer der anderen Lockerungsfunktionen, basierend auf der Übergangszeit. Das heißt, je kürzer die Übergangszeit ist, desto höher wird die Lockerungsfunktion zur Beschleunigung des Beschleunigungs- bzw. Verzögerungseffekts eingesetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
