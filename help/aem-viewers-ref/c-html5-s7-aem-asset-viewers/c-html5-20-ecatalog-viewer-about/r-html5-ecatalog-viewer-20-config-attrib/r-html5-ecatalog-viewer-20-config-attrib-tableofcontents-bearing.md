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
   <td> <p> Steuert die Richtung der Darstellung des Dropdown-Bedienfelds. </p> <p>Bei <span class="codeph"> Einstellung „Vertikal anpassen</span> verschiebt die Komponente zunächst die Position des Basisbereichs bis zum unteren Rand ihrer Schaltfläche und versucht, das Bedienfeld entweder rechts oder links von der Basisposition aus zu rollen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten ist. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbereichs nach oben zu verschieben und Rollout-Versuche in der rechten und linken Richtung zu wiederholen. </p> <p>Bei Einstellung von <span class="codeph">Seitenausrichtung</span> verwendet die Komponente eine ähnliche Logik, verschiebt aber den Fuß zuerst nach rechts und versucht Rollout-Richtungen nach unten und oben. Dann wird der Sockel nach links verschoben, es wird nach unten und oben gerollt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Legt die Verzögerung in Sekunden für den Dropdown-Zeitgeber zum automatischen Ausblenden fest, der das Bedienfeld ausblendet, wenn Benutzende inaktiv sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-55436ddd78b04f538dbb9a7a8463feae}

Optional.

## Standard {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Beispiel {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
