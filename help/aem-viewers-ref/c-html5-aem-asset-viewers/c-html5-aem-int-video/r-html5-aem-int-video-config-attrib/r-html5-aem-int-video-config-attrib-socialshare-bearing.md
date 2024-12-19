---
title: SocialShare.bearing
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oben|unten|links|rechts|vertikal|seitlich anpassen</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für Schaltflächen-Container an. Wenn auf <span class="codeph">up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> oder <span class="codeph"> right</span> eingestellt, wird das Bedienfeld in die angegebene Richtung ohne zusätzliche Begrenzungsprüfung ausgerollt, was dazu führen kann, dass das Bedienfeld von einem externen Container abgeschnitten wird. </p> <p>Bei Festlegung auf <span class="codeph"> Anpassen-</span> verschiebt die Komponente zunächst die Position des Basispanels nach unten in SocialShare. Anschließend wird versucht, das Bedienfeld in einer der folgenden Richtungen von einem solchen Basisspeicherort aus einzuführen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basispanels nach oben zu verschieben und die Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Bei Einstellung von <span class="codeph">Seitenausrichtung</span> verwendet die Komponente eine ähnliche Logik, verschiebt jedoch den Fuß zuerst nach rechts, versucht es in den Rollout-Richtungen nach rechts, unten und oben. Dann wird der Sockel nach links verschoben und versucht nach links, unten und oben in Rollout-Richtungen. </p> </td> 
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
