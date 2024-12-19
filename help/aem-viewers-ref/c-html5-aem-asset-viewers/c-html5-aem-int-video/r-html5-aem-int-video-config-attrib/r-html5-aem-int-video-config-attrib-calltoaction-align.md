---
title: CallToAction.align
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a92c4a-3757-4811-87b8-68fb367ea94d
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# CallToAction.align{#calltoaction-align}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]align=left|center|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links|Mitte|rechts</span> </p> </td> 
   <td colname="col2"> <p> Gibt die interne horizontale Ausrichtung (oder Verankerung) des Miniatur-Containers im Komponentenbereich an. </p> <p>Bei einem Aktionsaufruf wird der interne Miniatur-Container so dimensioniert, dass nur eine ganze Anzahl von Miniaturen angezeigt wird. Infolgedessen gibt es einen gewissen Abstand zwischen dem internen Container und den Begrenzungen der externen Komponente. </p> <p>Dieser Modifikator gibt an, wie der Container Interne Miniaturen horizontal innerhalb der Komponente positioniert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`center`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
align=left
```
