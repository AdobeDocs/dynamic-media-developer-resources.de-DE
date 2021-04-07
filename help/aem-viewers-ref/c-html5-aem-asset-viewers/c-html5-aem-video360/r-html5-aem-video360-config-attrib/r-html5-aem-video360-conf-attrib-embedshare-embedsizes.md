---
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
title: EmbedShare.embedsizes
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
exl-id: 3a6c23dd-5e2c-4149-aa24-37d445128125
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 10%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Konfigurationsattribut für Video360 Viewer.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`widthheight`*[,0|1]]`

Gibt eine Liste der Einbettungsgrößen für das Kombinationsfeld &quot;Größe&quot;im Dialogfeld &quot;Freigabe einbetten&quot;an.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Breite einbetten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Einbettung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, ob dieses Element der Liste zunächst im Kombinationsfeld vorausgewählt werden soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
