---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
feature: Dynamic Media Classic, Viewer, SDK/API, Inline-Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---


# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`Dauer`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> Gibt den Typ des Effekts an, der bei einer Asset-Änderung auf die Haupt-Ansicht angewendet wird. </p> <p><span class="codeph"> Ohne Transition </span> erfolgt eine Änderung der Ansicht sofort. </p> <p><span class="codeph"> Deaktiviert </span> die Überblendungsfunktion, bei der das alte Bild ausgeblendet und das neue Bild eingeblendet wird. </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der Animation dauert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

Keine.

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
