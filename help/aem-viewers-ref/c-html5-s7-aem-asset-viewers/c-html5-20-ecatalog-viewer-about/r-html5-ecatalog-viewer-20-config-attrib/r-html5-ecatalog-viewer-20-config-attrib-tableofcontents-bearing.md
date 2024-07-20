---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Steuert die Richtung des Dropdown-Bedienfeldaussehens. </p> <p>Wenn der Wert auf <span class="codeph"> fit-vertical</span> gesetzt ist, verschiebt die Komponente zunächst die Position des Basisbedienfelds an den unteren Rand ihrer Schaltfläche und versucht, das Bedienfeld entweder rechts oder links vom Basisstandort auszurollen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld durch einen externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und wiederholt Rollout-Versuche in die rechte und linke Richtung. </p> <p>Wenn der Wert auf <span class="codeph"> fit-lateral</span> festgelegt ist, verwendet die Komponente eine ähnliche Logik, verschiebt jedoch zuerst die Basis nach rechts, versucht dann die Rollout-Richtung herunter und nach oben. Anschließend verschiebt er die Basis nach links, versucht die Rollout-Richtung nach unten und nach oben zu verschieben. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Legt die Verzögerung in Sekunden für den Zeitgeber für das automatische Ausblenden fest, der das Bedienfeld ausblendet, wenn ein Benutzer inaktiv ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-55436ddd78b04f538dbb9a7a8463feae}

Optional.

## Standard {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Beispiel {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
