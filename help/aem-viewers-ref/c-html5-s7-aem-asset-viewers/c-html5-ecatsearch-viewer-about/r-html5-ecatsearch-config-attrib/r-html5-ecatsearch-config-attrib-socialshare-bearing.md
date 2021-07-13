---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächencontainer an. </p> <p> Wenn <span class="codeph"> nach oben </span>, <span class="codeph"> nach unten </span>, <span class="codeph"> nach links </span> oder <span class="codeph"> nach rechts </span> eingestellt ist, wird das Bedienfeld in eine angegebene Richtung ohne zusätzliche Begrenzungsprüfung ausgefüllt. Dieses Verhalten kann dazu führen, dass der Bereich durch einen externen Container beschnitten wird. </p> <p>Wenn der Wert auf <span class="codeph"> fit-vertical </span> festgelegt ist, verschiebt die Komponente zunächst die Position des Bedienfelds auf den unteren Rand von SocialShare und versucht, das Bedienfeld von unten, rechts oder links von dieser Basisposition aus einzurollen. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Wenn die Komponente auf <span class="codeph"> fit-lateral </span> festgelegt ist, verwendet sie eine ähnliche Logik wie bei fit-vertical, verschiebt jedoch die Basis in das erste Mal nach rechts, nach unten und nach oben rollen die Richtungen aus. Anschließend verschiebt sie die Basis nach links, versucht nach links, nach unten und nach oben Rollout-Anweisungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Beispiel {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
