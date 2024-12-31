---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3cb91483-de8c-4d5c-9b46-7026c5001f3a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Gibt die interne Ausrichtung (Verankerung) des Farbfeld-Containers im Komponentenbereich an. In Farbfeldern ist der interne Miniatur-Container so dimensioniert, dass nur eine ganze Anzahl von Farbfeldern angezeigt wird. Infolgedessen gibt es einen gewissen Abstand zwischen den Begrenzungen des internen Containers und der externen Komponente. Dieser Befehl gibt an, wie der interne Farbfeld-Container innerhalb der Komponente positioniert wird.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> links|Mitte|rechts</span> </p> </td> 
   <td> <p> Legt die Ausrichtung der horizontalen Farbfelder fest. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> oben|Mitte|unten</span> </p> </td> 
   <td> <p> Legt die Ausrichtung der vertikalen Farbfelder fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`center,center`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
