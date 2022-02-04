---
title: SocialShare.bearing
description: Konfigurationsattribut für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut für Video-Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächencontainer an. </p> <p> Wenn auf <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>oder <span class="codeph"> right</span>, bewegt sich das Bedienfeld in eine angegebene Richtung ohne zusätzliche Begrenzungsprüfung, was dazu führen kann, dass der Bedienfeld durch einen externen Container beschnitten wird. </p> <p>Wenn auf <span class="codeph"> fit-vertical</span>, verschiebt die Komponente zunächst die Position des Basisbedienfelds nach unten von SocialShare und versucht, das Bedienfeld von unten, rechts oder links von diesem Basisspeicherort auszurollen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld durch einen externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt Rollout-Versuche in die obere, rechte und linke Richtung. </p> <p>Wenn auf <span class="codeph"> fit-lateral</span>verwendet die Komponente eine ähnliche Logik. Er verschiebt jedoch zuerst die Basis nach rechts, versucht nach rechts, nach unten und nach oben, bewegt dann die Basis nach links, versucht nach links, nach unten und nach oben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
