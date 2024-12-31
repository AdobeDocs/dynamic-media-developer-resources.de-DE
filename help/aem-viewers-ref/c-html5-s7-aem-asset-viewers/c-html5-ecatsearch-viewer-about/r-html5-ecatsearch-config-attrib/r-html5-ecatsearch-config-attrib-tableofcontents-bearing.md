---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Steuert die Richtung der Darstellung des Dropdown-Bedienfelds. </p> <p>Bei <span class="codeph"> Einstellung „Vertikal anpassen</span> verschiebt die Komponente zunächst die Position des Basisbereichs bis zum unteren Rand ihrer Schaltfläche und versucht, das Bedienfeld von der Basisposition entweder nach rechts oder nach links auszurollen. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld von einem externen Container abgeschnitten ist. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basispanels nach oben zu verschieben und Rollout-Versuche in der rechten und linken Richtung zu wiederholen. </p> <p>Bei Einstellung <span class="codeph"> „Seitlich anpassen</span> verwendet die Komponente eine ähnliche Logik, verschiebt aber die Basis zuerst nach rechts, indem sie nach unten und oben rollt. Dann wird die Basis nach links verschoben, man versucht nach unten und nach oben zu rollen. </p> </td> 
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

[!DNL `fit-vertical,2`]

## Beispiel {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
