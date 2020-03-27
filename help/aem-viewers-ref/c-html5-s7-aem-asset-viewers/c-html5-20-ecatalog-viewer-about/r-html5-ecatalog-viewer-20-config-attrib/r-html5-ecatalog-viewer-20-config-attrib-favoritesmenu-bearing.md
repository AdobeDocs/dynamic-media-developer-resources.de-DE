---
description: Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an.
seo-description: Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an.
seo-title: FavoritesMenu.lager
solution: Experience Manager
title: FavoritesMenu.lager
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesMenu.lager{#favoritesmenu-bearing}

Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Wenn das Bedienfeld auf " <span class="codeph"> Nach oben</span>", " <span class="codeph"> Nach unten</span>", " <span class="codeph"> Nach links</span>"oder " <span class="codeph"> Nach rechts</span>"eingestellt ist, wird es ohne zusätzliche Begrenzungsüberprüfung in eine bestimmte Richtung ausgeführt, was dazu führt, dass der Bereich durch einen äußeren Container beschnitten wird. </p> <p>Wenn die Komponente auf <span class="codeph"> vertikal</span>anpassen eingestellt ist, verschiebt sie zunächst die Position des Basisbedienfelds an den unteren Rand des Favoritenmenüs und versucht, das Bedienfeld in einer der folgenden Richtungen von dieser Basisposition aus auszurollen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche von oben nach rechts und links zu wiederholen. </p> <p>Bei Festlegung auf <span class="codeph"> seitliche</span>Anpassung verwendet die Komponente eine ähnliche Logik. Die Basis wird zuerst nach rechts verschoben und versucht nach rechts, nach unten und nach oben auszurollen. Dann verschiebt es die Basis nach links und versucht nach links, nach unten und nach oben auszurollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
