---
description: Swatches.align
solution: Experience Manager
title: Swatches.align
feature: Dynamic Media Classic, Viewer, SDK/API, Inline-Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Gibt die interne Ausrichtung (Verankerung) des Containers &quot;Muster&quot;im Komponentenbereich an. Bei Farbfeldern wird der Container für die Miniaturansicht so angepasst, dass nur eine ganze Anzahl von Farbfeldern angezeigt wird. Das führt dazu, dass zwischen dem internen Container und den externen Komponentengrenzen eine gewisse Auffüllung besteht. Dieser Befehl gibt an, wie der Container für interne Farbfelder innerhalb der Komponente positioniert wird.

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> Legt die Ausrichtung der horizontalen Muster fest. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td colname="col2"> <p> Legt die Ausrichtung der vertikalen Farbfelder fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`center,center`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`align=left,top`
