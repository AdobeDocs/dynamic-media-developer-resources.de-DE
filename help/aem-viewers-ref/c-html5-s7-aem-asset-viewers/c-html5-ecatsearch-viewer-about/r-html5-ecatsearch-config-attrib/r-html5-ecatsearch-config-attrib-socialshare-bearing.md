---
description: SocialShare.Bearing
solution: Experience Manager
title: SocialShare.Bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
TQID: 'https://experienceleague.adobe.com/YQHHEkxD3goTHedA78xWDI59PaHnM-vOMdjcBa3TNq8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 1%

---

# SocialShare.Bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oben|unten|links|rechts|vertikal|seitlich anpassen</span> </p> </td> 
   <td colname="col2"> <p> Gibt die Richtung der Folienanimation für den Schaltflächen-Container an. </p> <p> Wenn die Option </span> <span class="codeph">, </span> nach unten <span class="codeph">, </span> nach <span class="codeph"> oder </span> nach <span class="codeph"> festgelegt wird, wird der Bereich ohne zusätzliche Begrenzungsprüfung in eine bestimmte Richtung ausgerollt. Dieses Verhalten kann dazu führen, dass Bedienfelder durch einen externen Container abgeschnitten werden. </p> <p>Bei Festlegung auf <span class="codeph"> vertikale </span> verschiebt die Komponente zunächst die Position des Basispanels nach unten in SocialShare und versucht, das Bedienfeld entweder von unten, rechts oder links von dieser Basisposition aus einzuführen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbereichs nach oben zu verschieben und die Rollout-Versuche von oben, rechts und links zu wiederholen. </p> <p>Bei der Einstellung "<span class="codeph"> </span>-Seitenausrichtung“ verwendet die Komponente eine ähnliche Logik wie bei „Anpassen-Vertikal“, verschiebt jedoch die Basis nach rechts, zuerst nach rechts, nach unten und nach oben und verschiebt dann die Basis nach links, versucht nach links, nach unten und nach oben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Beispiel {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
