---
description: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Aktiviert die Anzeige des IconEffect über dem Video, wenn das Video angehalten wird. Auf einigen Geräten werden native Steuerelemente verwendet. In diesem Fall wird der Modifikator <span class="codeph"> iconeffect</span> ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft IconEffect maximal angezeigt und wieder angezeigt wird. Der Wert <span class="codeph"> -1</span> gibt an, dass das Symbol unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> verblassen</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Anzahl der Sekunden fest, die der IconEffect sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach dem Einblenden der Animation und vor dem Ausblenden der Animation ist abgelaufen. Eine Einstellung von <span class="codeph"> 0</span> deaktiviert das automatische Ausblenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
