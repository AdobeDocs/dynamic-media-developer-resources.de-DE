---
title: SocialShare.Bearing
description: Konfigurationsattribut für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
TQID: 'https://experienceleague.adobe.com/YhNrijfrkxHpLzZFMRr2AdjFARJ8E5xSaTfhANHbXGo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 1%

---

# SocialShare.Bearing{#socialshare-bearing}

Konfigurationsattribut für Video Viewer.

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
