---
title: Navigation
description: URL-Befehl für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
TQID: 'https://experienceleague.adobe.com/9NeyqqTJGWW9Owp8MR8MguU5lFSJrdY0rteZZVoRwY4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 10%

---

# Navigation{#navigation}

URL-Befehl für den interaktiven Video-Viewer.

` navigation= *`Datei`*`

Der Viewer unterstützt die Videokapitelnavigation mithilfe von gehosteten WebVTT-Dateien. Cue-Point-Positionierungsoperatoren werden nicht unterstützt.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Datei</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Navigationsinhalt an. Image Serving sollte die WebVTT-Datei hosten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
