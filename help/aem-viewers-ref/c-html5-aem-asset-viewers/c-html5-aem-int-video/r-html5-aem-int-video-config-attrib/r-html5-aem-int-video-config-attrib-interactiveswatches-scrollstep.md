---
title: InteractiveSwatches.scrollstep
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Konfigurationsattribut für interaktiven Video-Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`Schritt`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Anzahl der Farbfelder an, die bei jedem Tippen auf die entsprechende Bildlaufschaltfläche gescrollt werden sollen. </p> <p>Wenn der angegebene Wert größer ist als die Anzahl der sichtbaren interaktiven Muster, wird bei jedem Tippen nur nach der Anzahl der sichtbaren Farbfelder gescrollt, um zu verhindern, dass ein Farbmuster weggelassen wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`3`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
