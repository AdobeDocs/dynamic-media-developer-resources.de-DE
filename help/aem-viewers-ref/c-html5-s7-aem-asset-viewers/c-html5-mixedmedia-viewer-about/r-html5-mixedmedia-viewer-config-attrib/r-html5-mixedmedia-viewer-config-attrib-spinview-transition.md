---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`time`*[, *`Lockerung`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zeit</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die die Animation für die Aktion eines einzelnen Zoomschritts benötigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Lockerung</span></span> </p> </td> 
   <td colname="col2"> <p> Erstellt eine Illusion der Beschleunigung oder Verzögerung, die den Übergang natürlicher erscheinen lässt. Sie können die Lockerung auf eine der folgenden Optionen einstellen: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (auto) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linear) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratisch) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (kubisch) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (Quartil) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintisch) </li> 
     </ul> </p> <p>Der Auto-Modus verwendet immer einen linearen Übergang, wenn der elastische Zoom deaktiviert ist (Standard). Andernfalls passt es zu einer der anderen Erleichterungsfunktionen, die auf der Übergangszeit basieren. Das heißt, je kürzer die Übergangszeit ist, desto höher wird die Lockerungsfunktion verwendet, um den Beschleunigungs- oder Verzögerungseffekt zu beschleunigen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
