---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Steuert die Richtung des Dropdown-Bedienfeldaussehens. </p> <p>Wenn der Wert auf <span class="codeph"> fit-vertical</span> festgelegt ist, verschiebt die Komponente zunächst die Position des Bedienfelds am unteren Rand der Schaltfläche und versucht, das Bedienfeld von der Basisposition entweder nach rechts oder nach links zu verschieben. Bei jedem Versuch prüft die Komponente, ob das Bedienfeld durch einen externen Container beschnitten wird. Wenn alle Versuche fehlschlagen, versucht die Komponente, die Position des Basisbedienfelds nach oben zu verschieben und die Rollout-Versuche in die rechte und linke Richtung zu wiederholen. </p> <p>Wenn der Wert auf <span class="codeph"> fit-lateral</span> festgelegt ist, verwendet die Komponente eine ähnliche Logik, verschiebt jedoch zuerst die Basis nach rechts, versucht nach unten und nach oben Rollout-Anweisungen. Dann wechselt er die Basis nach links, versucht nach unten und nach oben, die Richtung einzuführen. </p> </td> 
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

[!DNL `fit-vertical,2`]

## Beispiel {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
