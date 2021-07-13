---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut für interaktiven Video-Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für Schaltflächencontainer an. Wenn der Wert auf <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> oder <span class="codeph"> right</span> festgelegt ist, wird das Bedienfeld in die angegebene Richtung ausgefüllt, ohne dass zusätzliche Begrenzungen überprüft werden, was dazu führen kann, dass das Bedienfeld durch einen externen Container beschnitten wird. </p> <p>Wenn der Wert auf <span class="codeph"> fit-vertical</span> festgelegt ist, verschiebt die Komponente zunächst die Position des Basisbedienfelds an den unteren Rand von SocialShare und versucht, das Bedienfeld in eine der folgenden Richtungen von einem solchen Basisspeicherort aus einzuführen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob der Bereich durch einen externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt die Rollout-Versuche von oben, rechts und links. </p> <p>Wenn der Wert auf <span class="codeph"> fit-lateral</span> festgelegt ist, verwendet die Komponente eine ähnliche Logik, verschiebt jedoch zuerst die Basis nach rechts, versucht dann nach rechts, nach unten und nach oben zu bewegen. Anschließend verschiebt er die Basis nach links, versucht nach links, nach unten und nach oben die Rollout-Richtung. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
