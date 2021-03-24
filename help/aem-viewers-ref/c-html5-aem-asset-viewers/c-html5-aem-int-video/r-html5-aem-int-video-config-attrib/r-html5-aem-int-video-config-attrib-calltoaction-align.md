---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.align
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---


# CallToAction.align{#calltoaction-align}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]align=left|center|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> Gibt die interne horizontale Ausrichtung (oder Verankerung) des Miniaturansichten-Containers im Komponentenbereich an. </p> <p>Beim Aktionsaufruf wird die Größe des internen Miniaturbilds so angepasst, dass nur eine ganze Anzahl von Miniaturbildern angezeigt wird. Das führt dazu, dass zwischen dem internen Container und den externen Komponentengrenzen eine gewisse Auffüllung besteht. </p> <p>Dieser Modifikator gibt an, wie der Container für interne Miniaturansichten horizontal in der Komponente positioniert wird. </p> </td> 
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

