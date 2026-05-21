---
title: Video360Player.iconeffect
description: Konfigurationsattribut für Video360-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
TQID: 'https://experienceleague.adobe.com/hi-8zIddM3Pybmh38PWiMSYuSY5COz9FnJpZs3FJ6yE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 3%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Konfigurationsattribut für Video360-Viewer.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Ermöglicht die Anzeige von IconEffect über dem Video, wenn das Video angehalten wurde. Auf einigen Geräten werden systemeigene Steuerelemente verwendet. In solchen Fällen wird der <span class="codeph">iconeffect</span>-Modifikator ignoriert. </p> </td> 
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
