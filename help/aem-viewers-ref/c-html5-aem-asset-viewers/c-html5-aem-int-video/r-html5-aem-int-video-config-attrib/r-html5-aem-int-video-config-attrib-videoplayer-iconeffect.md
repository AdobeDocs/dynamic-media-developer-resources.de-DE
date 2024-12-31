---
title: VideoPlayer.iconeffect
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Ermöglicht die Anzeige von IconEffect über dem Video, wenn das Video angehalten wurde. Auf einigen Geräten werden systemeigene Steuerelemente verwendet. In solchen Fällen wird der Modifikator <span class="codeph">iconeffect</span> ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Anzahl</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft IconEffect maximal angezeigt und wieder angezeigt werden soll. Der Wert <span class="codeph"> -1</span> bedeutet, dass das Symbol unbegrenzt erneut angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> verblasst</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> automatisch ausblenden</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die Anzahl der Sekunden fest, die der IconEffect vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach Abschluss des Einblendens der Animation und vor Beginn des Ausblendevorgangs. Auf <span class="codeph"> 0</span> setzen, um das automatische Ausblenden zu deaktivieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
