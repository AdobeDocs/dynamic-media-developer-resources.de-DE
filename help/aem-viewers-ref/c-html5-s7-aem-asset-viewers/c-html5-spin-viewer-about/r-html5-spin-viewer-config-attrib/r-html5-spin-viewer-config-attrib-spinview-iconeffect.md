---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
topic: Dynamic media
uuid: 864fb8dc-34f8-4216-b38c-cc00f7d8d95f
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert die Anzeige des <span class="codeph">-Iconeffect</span> oben im Bild, wenn sich das Bild in einem Reset-Status befindet und eine verfügbare Aktion für die Interaktion mit dem Bild angezeigt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft <span class="codeph"> der Iconeffect</span> maximal angezeigt und erneut angezeigt wird. Der Wert <span class="codeph"> -1</span> gibt an, dass das Symbol immer unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, in denen der <span class="codeph">-Iconeffect</span> vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach Abschluss der Einblendeanimation, aber vor dem Ausblenden der Beginn. Die Einstellung <span class="codeph"> 0</span> deaktiviert das automatische Ausblenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
