---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---


# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`Zeitbeschleunigung `*[, *``*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zeit</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für eine einzelne Zoomschritt-Aktion dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> lockern</span></span> </p> </td> 
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

## Eigenschaften {#section-ebfd9162c8504666bf0e4485bf3b1383}

Optional.

## Standard {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## Beispiel {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
