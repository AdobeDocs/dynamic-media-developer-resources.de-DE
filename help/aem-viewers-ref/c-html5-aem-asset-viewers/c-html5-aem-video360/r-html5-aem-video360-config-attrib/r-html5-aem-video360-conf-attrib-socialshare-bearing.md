---
title: SocialShare.bearing
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut für Video360 Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächencontainer an. </p> <p> Wenn der Wert auf <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> oder <span class="codeph"> right</span> festgelegt ist, wird das Bedienfeld in eine angegebene Richtung ohne zusätzliche Begrenzungsprüfung ausgeführt, was dazu führen kann, dass der Bedienfeld durch einen externen Container beschnitten wird. </p> <p>Wenn der Wert auf <span class="codeph"> fit-vertical</span> festgelegt ist, verschiebt die Komponente zunächst die Position des Basisbereichs nach unten von SocialShare und versucht, das Bedienfeld von unten, rechts oder links von dieser Basisposition aus einzurollen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld durch einen externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt Rollout-Versuche in die obere, rechte und linke Richtung. </p> <p>Wenn der Wert auf <span class="codeph"> fit-lateral</span> festgelegt ist, verwendet die Komponente eine ähnliche Logik. Er verschiebt jedoch zuerst die Basis nach rechts, versucht nach rechts, nach unten und nach oben, bewegt dann die Basis nach links, versucht nach links, nach unten und nach oben. </p> </td> 
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
