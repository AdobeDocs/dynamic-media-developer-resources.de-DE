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
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächencontainer an. </p> <p> Wenn auf <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span>oder <span class="codeph"> right </span>, wird das Bedienfeld in eine angegebene Richtung ohne zusätzliche Begrenzungsprüfung ausgeführt. Dieses Verhalten kann dazu führen, dass der Bereich durch einen externen Container beschnitten wird. </p> <p>Wenn auf <span class="codeph"> fit-vertical </span>, verschiebt die Komponente zunächst die Position des Basisbedienfelds nach unten von SocialShare und versucht, das Bedienfeld von diesem Basisspeicherort aus entweder von unten, rechts oder links auszurollen. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Wenn auf <span class="codeph"> fit-lateral </span>verwendet die Komponente eine ähnliche Logik wie bei fit-vertical. Er verschiebt die Basis jedoch nach rechts, zuerst nach rechts, nach unten und nach oben, um die Richtungen nach links zu verschieben. Anschließend verschiebt er die Basis nach links, versucht nach links, nach unten und nach oben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Beispiel {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
