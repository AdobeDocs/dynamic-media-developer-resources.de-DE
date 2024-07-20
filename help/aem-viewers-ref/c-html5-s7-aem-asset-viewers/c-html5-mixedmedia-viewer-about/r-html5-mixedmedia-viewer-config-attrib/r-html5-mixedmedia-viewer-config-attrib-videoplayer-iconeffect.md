---
title: VideoPlayer.iconeffect
description: VideoPlayer.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 8371cb69-4cd9-457b-bd8c-e4167fc67600
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Aktiviert den "IconEffect", damit er über dem Video angezeigt wird, wenn das Video angehalten wird. Auf einigen Geräten werden native Steuerelemente verwendet. In diesem Fall wird der Modifikator <span class="codeph"> iconEffect</span> ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft IconEffect maximal angezeigt und wieder angezeigt wird. Der Wert <span class="codeph"> -1</span> zeigt an, dass das Symbol auf unbestimmte Zeit wieder angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Legt fest, wie viele Sekunden der IconEffect sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach dem Einblenden der Animation und vor dem Ausblenden der Animation. Die Einstellung "<span class="codeph"> 0</span>" deaktiviert das automatische Ausblendeverhalten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
