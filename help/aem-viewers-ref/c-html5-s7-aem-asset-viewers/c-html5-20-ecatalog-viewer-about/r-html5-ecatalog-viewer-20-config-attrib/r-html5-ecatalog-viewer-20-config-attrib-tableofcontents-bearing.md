---
description: 'null'
seo-description: 'null'
seo-title: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 791aaaa5-3777-4f68-a445-caa3d975d883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Steuert die Richtung der Darstellung des Dropdown-Bedienfelds. </p> <p>Bei Festlegung auf <span class="codeph"> fit-vertical</span> verschiebt die Komponente zunächst die Position des Basispanels an den unteren Rand der Schaltfläche und versucht, das Bedienfeld von der Basisposition nach rechts oder links zu verschieben. Bei jedem Versuch prüft die Komponente, ob der Bereich von einem externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche nach rechts und links zu wiederholen. </p> <p>Bei Festlegung auf <span class="codeph"> fit-lateral</span> verwendet die Komponente eine ähnliche Logik, verschiebt die Basis jedoch zunächst nach rechts und versucht dabei, die Richtung nach unten und nach oben auszurollen. Dann verschiebt es die Basis nach links, versucht die Richtung nach unten und nach oben auszurollen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Legt die Verzögerung in Sekunden für den Dropdown-Zeitgeber für das automatische Ausblenden fest, mit dem der Bereich ausgeblendet wird, wenn sich ein Benutzer im Leerlauf befindet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-55436ddd78b04f538dbb9a7a8463feae}

Optional.

## Standard {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Beispiel {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
