---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: SocialShare.lager
solution: Experience Manager
title: SocialShare.lager
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialShare.lager{#socialshare-bearing}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Diashow-Animation für den Container "Schaltflächen"an. Wenn das Bedienfeld auf <span class="codeph"> oben</span>, <span class="codeph"> unten</span>, <span class="codeph"> links</span>oder <span class="codeph"> rechts</span>eingestellt ist, wird es ohne zusätzliche Begrenzungsüberprüfung in die angegebene Richtung ausgeführt, was dazu führen kann, dass das Bedienfeld von einem äußeren Container abgeschnitten wird. </p> <p>Wenn die Komponente auf " <span class="codeph"> An-Vertikal</span>anpassen"eingestellt ist, verschiebt sie zunächst die Position des Basisbedienfelds an den unteren Rand von SocialShare und versucht, das Bedienfeld in eine der folgenden Richtungen von einem solchen Basisspeicherort aus auszurollen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt die Rollout-Versuche von oben nach rechts und links. </p> <p>Wenn die Komponente auf <span class="codeph"> seitliche</span>Anpassung eingestellt ist, verwendet sie eine ähnliche Logik, verschiebt die Basis jedoch zuerst nach rechts, versucht nach rechts, nach unten und nach oben. Anschließend wird die Basis nach links verschoben und es wird nach links, nach unten und nach oben gewechselt. </p> </td> 
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

