---
description: Konfigurationsattribut für Video Viewer.
seo-description: Konfigurationsattribut für Video Viewer.
seo-title: SocialShare.lager
solution: Experience Manager
title: SocialShare.lager
topic: Dynamic media
uuid: d7d92d63-a4c2-4bd9-b0fd-fdfd47504a39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.lager{#socialshare-bearing}

Konfigurationsattribut für Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an. </p> <p> Wenn das Bedienfeld auf <span class="codeph"> oben</span>, <span class="codeph"> unten</span>, <span class="codeph"> links</span>oder <span class="codeph"> rechts</span>eingestellt ist, wird es ohne zusätzliche Begrenzungsüberprüfung in eine angegebene Richtung ausgeführt, was dazu führen kann, dass der Bedienfeld durch einen äußeren Container beschnitten wird. </p> <p>Wenn diese Einstellung auf <span class="codeph"> vertikal</span>angepasst ist, verschiebt die Komponente zunächst die Position des Basisbedienfelds an den unteren Rand von SocialShare und versucht, das Bedienfeld von unten, rechts oder links von dieser Position aus auszurollen. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche in die obere, rechte und linke Richtung zu wiederholen. </p> <p>Bei Festlegung auf <span class="codeph"> seitliche</span>Anpassung verwendet die Komponente eine ähnliche Logik. Die Basis wird jedoch zuerst nach rechts verschoben, dann versucht es nach rechts, nach unten und nach oben. Anschließend wird die Basis nach links verschoben und es wird nach links, nach unten und nach oben gewechselt. </p> </td> 
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

