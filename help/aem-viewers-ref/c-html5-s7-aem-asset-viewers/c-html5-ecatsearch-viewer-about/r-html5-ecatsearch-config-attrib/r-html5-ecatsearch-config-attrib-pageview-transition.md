---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e9db5c83-e6cf-4847-99b3-a1cf6a1fbe9f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# PageView.transition{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *`time`*[, *`easing`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zeit</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für einen einzelnen Zoom-Schritt ausführen soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Erleichterung</span></span> </p> </td> 
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

## Eigenschaften {#section-ebfd9162c8504666bf0e4485bf3b1383}

Optional.

## Standard {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## Beispiel {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
