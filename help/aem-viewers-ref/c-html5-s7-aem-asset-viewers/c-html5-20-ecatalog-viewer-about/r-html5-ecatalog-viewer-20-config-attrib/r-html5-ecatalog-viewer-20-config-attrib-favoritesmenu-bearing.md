---
title: FavoritesMenu.bearing
description: Gibt die Richtung der Folienanimation für den Schaltflächencontainer an.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Gibt die Richtung der Folienanimation für den Schaltflächencontainer an.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Wenn auf <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>oder <span class="codeph"> right</span>, bewegt sich das Bedienfeld in die angegebene Richtung ohne zusätzliche Begrenzungsprüfung, was dazu führt, dass der Bedienfeld durch einen externen Container beschnitten wird. </p> <p>Wenn auf <span class="codeph"> fit-vertical</span>, verschiebt die Komponente zunächst die Position des Basisbedienfelds auf den unteren Rand des Favoriten-Menüs. Es wird versucht, das Bedienfeld in eine der folgenden Richtungen von diesem Basisspeicherort aus einzuführen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld durch einen externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Wenn auf <span class="codeph"> fit-lateral</span>verwendet die Komponente eine ähnliche Logik. Die Basis wird zuerst nach rechts verschoben und versucht nach rechts, nach unten und nach oben zu rollen. Dann wechselt er die Basis nach links, versucht nach links, nach unten und nach oben, die Richtung zu verschieben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
