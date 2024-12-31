---
title: SocialShare.bearing
description: Konfigurationsattribut für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut für den Smart Crop Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oben|unten|links|rechts|vertikal|seitlich anpassen</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächen-Container an. </p> <p> Bei <span class="codeph"> auf </span>, <span class="codeph"> nach unten</span>, <span class="codeph"> nach </span> oder <span class="codeph"> nach rechts</span> wird das Bedienfeld ohne zusätzliche Begrenzungsprüfung in eine bestimmte Richtung ausgerollt, was dazu führen kann, dass das Bedienfeld durch einen externen Container abgeschnitten wird. </p> <p>Bei Festlegung auf <span class="codeph">Anpassen vertikal</span> verschiebt die Komponente zunächst die Position des Basispanels nach unten in SocialShare und versucht, das Bedienfeld von diesem Basispunkt aus nach unten, rechts oder links auszuführen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten ist. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbereichs nach oben zu verschieben und Rollout-Versuche in die obere, rechte und linke Richtung zu wiederholen. </p> <p>Bei Festlegung auf "<span class="codeph">-lateral</span> verwendet die Komponente eine ähnliche Logik. Dabei wird die Basis jedoch zuerst nach rechts verschoben, wobei rechts, unten und oben die Rollout-Richtungen ausprobiert werden. Anschließend wird die Basis nach links verschoben, wobei links, unten und oben die Rollout-Richtungen ausprobiert werden. </p> </td> 
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
