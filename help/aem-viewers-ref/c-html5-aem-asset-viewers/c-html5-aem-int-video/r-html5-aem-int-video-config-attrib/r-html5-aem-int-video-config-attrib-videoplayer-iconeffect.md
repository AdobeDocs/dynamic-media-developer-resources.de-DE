---
title: VideoPlayer.iconeffect
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Konfigurationsattribut für interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`count`*][, *`verblassen`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert die Anzeige des IconEffect über dem Video, wenn das Video angehalten wird. Auf einigen Geräten werden native Steuerelemente verwendet. In diesen Fällen wird die <span class="codeph"> iconEffect</span> -Modifikator wird ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft IconEffect maximal angezeigt und wieder angezeigt wird. Ein Wert von <span class="codeph"> -1</span> gibt an, dass das Symbol unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Legt fest, wie viele Sekunden der IconEffect vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach dem Verblassen in der Animation und vor dem Beginn der Ausblendung. Legen Sie <span class="codeph"> 0</span> , um das automatische Ausblenden zu deaktivieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
