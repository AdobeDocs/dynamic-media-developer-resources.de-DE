---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oben|unten|links|rechts|vertikal|seitlich anpassen</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächen-Container an. </p> <p> Wenn auf <span class="codeph"> </span>, <span class="codeph"> nach unten </span>, <span class="codeph"> nach </span> oder <span class="codeph"> nach </span> festgelegt, wird das Bedienfeld ohne zusätzliche Begrenzungsprüfung in eine bestimmte Richtung ausgerollt. Dieses Verhalten kann dazu führen, dass Bedienfelder durch einen externen Container abgeschnitten werden. </p> <p>Bei Festlegung auf <span class="codeph"> vertikale </span> verschiebt die Komponente zunächst die Position des Basispanels nach unten in SocialShare und versucht, das Bedienfeld entweder von unten, rechts oder links von dieser Basisposition aus einzuführen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbereichs nach oben zu verschieben und die Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Bei <span class="codeph"> Einstellung „Seitliches </span> anpassen“ verwendet die Komponente eine ähnliche Logik wie bei „Vertikal anpassen“. Die Basis wird jedoch nach rechts verschoben, zuerst nach rechts, nach unten und nach oben. Anschließend wird die Basis nach links verschoben und nach links, nach unten und nach oben verschoben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Beispiel {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
