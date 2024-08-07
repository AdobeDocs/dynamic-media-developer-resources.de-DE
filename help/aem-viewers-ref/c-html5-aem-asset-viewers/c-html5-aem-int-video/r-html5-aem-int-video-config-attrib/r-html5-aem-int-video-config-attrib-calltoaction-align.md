---
title: CallToAction.align
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a92c4a-3757-4811-87b8-68fb367ea94d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# CallToAction.align{#calltoaction-align}

Konfigurationsattribut für interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]align=left|center|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> Gibt die interne horizontale Ausrichtung (oder Verankerung) des Containers für Miniaturansichten innerhalb des Komponentenbereichs an. </p> <p>Beim Aktionsaufruf wird der interne Miniaturansichtsbehälter so skaliert, dass nur eine ganze Anzahl von Miniaturansichten angezeigt wird. Infolgedessen besteht ein gewisser Abstand zwischen dem internen Container und den externen Komponentengrenzen. </p> <p>Dieser Modifikator gibt an, wie der interne Container für Miniaturansichten horizontal in der Komponente platziert wird. </p> </td> 
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
