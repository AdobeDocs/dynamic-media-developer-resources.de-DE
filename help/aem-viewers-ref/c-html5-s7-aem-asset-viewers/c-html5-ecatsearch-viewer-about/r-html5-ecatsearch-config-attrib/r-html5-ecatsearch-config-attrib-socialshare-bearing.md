---
description: 'null'
seo-description: 'null'
seo-title: SocialShare.lager
solution: Experience Manager
title: SocialShare.lager
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# SocialShare.lager{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Diashow-Animation für den Schaltflächen-Container an. </p> <p> Wenn das Bedienfeld so eingestellt ist, dass es <span class="codeph"> nach oben, </span>nach unten <span class="codeph"> , </span>links <span class="codeph"> oder </span><span class="codeph"> </span>rechts verläuft, wird es ohne zusätzliche Begrenzungsüberprüfung in eine angegebene Richtung ausgeführt. Dies kann dazu führen, dass der Bereich von einem externen Container beschnitten wird. </p> <p>Wenn die Komponente auf <span class="codeph"> </span>An-die-Vertikal-Einstellung eingestellt ist, verschiebt sie zunächst die Position des Basisbedienfelds an den unteren Rand von SocialShare und versucht, das Bedienfeld entweder von unten, rechts oder links von dieser Position aus auszurollen. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt die Rollout-Versuche von oben nach rechts und links. </p> <p>Bei Festlegung auf " <span class="codeph"> </span>passseitig"verwendet die Komponente eine ähnliche Logik wie bei "fit-vertical", verschiebt die Basis jedoch stattdessen nach rechts, zunächst nach rechts, nach unten und nach oben, um die Richtung nach links zu verschieben. Anschließend versucht sie nach links, nach unten und nach oben auszurollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Beispiel {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
