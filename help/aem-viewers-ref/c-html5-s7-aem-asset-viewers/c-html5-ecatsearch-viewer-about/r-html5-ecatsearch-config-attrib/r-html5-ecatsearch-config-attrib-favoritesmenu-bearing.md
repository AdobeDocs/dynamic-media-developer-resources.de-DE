---
description: Gibt die Richtung der Folienanimation für den Schaltflächen-Container an.
solution: Experience Manager
title: FavoritenMenü.Peilung
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
TQID: 'https://experienceleague.adobe.com/Pe9frhI8cmIorx5zE-cdC-frEP77UOksMwyM9PvUCdo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# FavoritenMenü.Peilung{#favoritesmenu-bearing}

Gibt die Richtung der Folienanimation für den Schaltflächen-Container an.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> oben|unten|links|rechts|vertikal|seitlich anpassen</span> </p> </td> 
   <td colname="col2"> <p> Wenn <span class="codeph"> auf </span>, <span class="codeph"> nach unten</span>, <span class="codeph"> nach </span> oder <span class="codeph"> nach rechts</span> eingestellt, wird das Bedienfeld ohne zusätzliche Begrenzungsprüfung in die angegebene Richtung ausgerollt, was dazu führt, dass das Bedienfeld durch einen externen Container abgeschnitten wird. </p> <p>Bei <span class="codeph"> Einstellung „Anpassen - Vertikal</span> verschiebt die Komponente zunächst die Position des Basispanels zum unteren Rand des Menüs „Favoriten“ und versucht, das Bedienfeld von dieser Position aus in eine der folgenden Richtungen zu rollen: unten, rechts, links. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten ist. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbereichs nach oben zu verschieben und Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Bei Festlegung auf "<span class="codeph">-lateral</span> verwendet die Komponente eine ähnliche Logik. Die Basis wird zuerst nach rechts verschoben und versucht nach rechts, nach unten und nach oben. Dann wird die Basis nach links verschoben, es wird links versucht, es wird nach unten und oben gerollt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
