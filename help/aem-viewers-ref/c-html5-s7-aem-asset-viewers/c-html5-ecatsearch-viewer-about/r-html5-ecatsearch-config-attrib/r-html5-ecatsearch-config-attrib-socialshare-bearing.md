---
description: 'null'
seo-description: 'null'
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an. </p> <p> Bei Festlegung auf <span class="codeph"> nach oben </span>, <span class="codeph"> nach unten </span>, <span class="codeph"> nach links </span> oder <span class="codeph"> nach rechts </span> wird das Bedienfeld in eine angegebene Richtung ohne zusätzliche Begrenzungsüberprüfung ausgeführt. Dies kann dazu führen, dass der Bereich von einem externen Container beschnitten wird. </p> <p>Bei Festlegung auf <span class="codeph"> fit-vertical </span> verschiebt die Komponente zuerst die Position des Bedienfelds am unteren Rand von SocialShare und versucht, das Bedienfeld entweder von unten, rechts oder links von dieser Position aus zu verschieben. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt die Rollout-Versuche von oben nach rechts und links. </p> <p>Bei Festlegung auf <span class="codeph"> fit-lateral </span> verwendet die Komponente eine ähnliche Logik wie bei fit-vertical, verschiebt die Basis jedoch stattdessen nach rechts, nach unten und nach oben, verschiebt die Basis nach links und versucht nach links, nach unten und nach oben, die Richtung des Roll-out zu ändern. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Beispiel {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
