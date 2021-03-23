---
description: Konfigurationsattribut für Video360 Viewer.
seo-description: Konfigurationsattribut für Video360 Viewer.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut für Video360 Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an. </p> <p> Bei Einstellung auf <span class="codeph"> nach oben</span>, <span class="codeph"> nach unten</span>, <span class="codeph"> links</span> oder <span class="codeph"> rechts</span> wird das Bedienfeld ohne zusätzliche Begrenzungsüberprüfung in eine angegebene Richtung ausgeführt, was dazu führen kann, dass das Bedienfeld durch einen externen Container beschnitten wird. </p> <p>Bei Festlegung auf <span class="codeph"> fit-vertical</span> verschiebt die Komponente zunächst die Position des Basisbedienfelds an den unteren Rand von SocialShare und versucht, das Bedienfeld von unten, rechts oder links von dieser Position aus auszurollen. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche in die obere, rechte und linke Richtung zu wiederholen. </p> <p>Bei Festlegung auf <span class="codeph"> fit-lateral</span> verwendet die Komponente eine ähnliche Logik. Die Basis wird jedoch zuerst nach rechts verschoben, dann versucht es nach rechts, nach unten und nach oben. Anschließend wird die Basis nach links verschoben und es wird nach links, nach unten und nach oben gewechselt. </p> </td> 
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

