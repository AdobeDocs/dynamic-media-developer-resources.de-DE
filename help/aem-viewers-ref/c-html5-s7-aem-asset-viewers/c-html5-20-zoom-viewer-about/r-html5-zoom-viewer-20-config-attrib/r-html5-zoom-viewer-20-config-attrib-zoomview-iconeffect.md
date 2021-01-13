---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 3c10e625-f789-4454-8898-b3f293aa49b7
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

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

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
