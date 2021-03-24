---
description: Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Bei Festlegung auf <span class="codeph"> nach oben</span>, <span class="codeph"> nach unten</span>, <span class="codeph"> links</span> oder <span class="codeph"> rechts</span> wird das Bedienfeld ohne zusätzliche Begrenzungsüberprüfung in die angegebene Richtung verschoben, was dazu führt, dass der Bereich durch einen äußeren Container beschnitten wird. </p> <p>Bei Festlegung auf <span class="codeph"> fit-vertical</span> verschiebt die Komponente zunächst die Position des Basisbedienfelds an den unteren Rand des Favoritenmenüs und versucht, das Bedienfeld in einer der folgenden Richtungen von dieser Basisposition aus auszurollen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche von oben nach rechts und links zu wiederholen. </p> <p>Bei Festlegung auf <span class="codeph"> fit-lateral</span> verwendet die Komponente eine ähnliche Logik. Die Basis wird zuerst nach rechts verschoben und versucht nach rechts, nach unten und nach oben auszurollen. Dann verschiebt es die Basis nach links und versucht nach links, nach unten und nach oben auszurollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
