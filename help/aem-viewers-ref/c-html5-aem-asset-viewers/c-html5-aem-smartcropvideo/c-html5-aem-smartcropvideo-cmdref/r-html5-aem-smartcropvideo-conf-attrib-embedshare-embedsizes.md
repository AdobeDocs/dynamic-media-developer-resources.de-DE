---
title: EmbedShare.embedsizes
description: Konfigurationsattribut für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c638d9fd-39bb-4baa-9b3a-99d9bc0307b5
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Konfigurationsattribut für den Smart Crop Video Viewer.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`width`*, *`height`*[,0|1][; *`width`*, *`height`*[,0|1]]`

Gibt eine Liste der Einbettungsgrößen für das Kombinationsfeld Größe im modalen Einbettungsfreigabedialogfeld an.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Breite </span> </span> </p> </td> 
   <td colname="col2"> <p> Breite einbetten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Höhe </span> </span> </p> </td> 
   <td colname="col2"> <p>Einbettungshöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, ob dieses Listenelement im Kombinationsfeld vorab ausgewählt werden soll. </p> </td> 
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
