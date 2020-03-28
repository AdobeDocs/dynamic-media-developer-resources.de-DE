---
description: 'null'
seo-description: 'null'
seo-title: SpinView.Transition
solution: Experience Manager
title: SpinView.Transition
topic: Dynamic media
uuid: d5cc319a-fb0b-41d3-a118-f00376a127e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.Transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`Zeitbeschleunigung`*[, *``*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zeit</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für eine einzelne Zoomschritt-Aktion dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> lockern</span></span> </p> </td> 
   <td colname="col2"> <p> Erstellt eine Illusion der Beschleunigung oder Verzögerung, die die Transition natürlicher erscheinen lässt. Sie können die Lockerung auf einen der folgenden einstellen: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (auto) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linear) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratisch) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (kubisch) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (Quartil) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (Chinesisch) </li> 
     </ul> </p> <p>Der automatische Modus verwendet immer eine lineare Transition, wenn der elastische Zoom deaktiviert ist (Standard). Andernfalls passt es zu einer der anderen Beschleunigungsfunktionen, die auf der Transition basieren. Das heißt, je kürzer die Transition ist, desto höher wird die Beschleunigungsfunktion verwendet, um den Beschleunigungs- oder Verzögerungseffekt zu beschleunigen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
