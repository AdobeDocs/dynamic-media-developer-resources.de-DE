---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: InteractiveSwatches.scrollstep
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 7%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`Schritt`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Schritt</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Anzahl der Farbfelder an, die bei jedem Tippen auf die entsprechende Bildlauftaste durchlaufen werden sollen. </p> <p>Wenn der angegebene Wert größer als die Anzahl der sichtbaren interaktiven Muster ist, wird bei jedem Tippen nur nach der Anzahl der sichtbaren Farbfelder geblättert, um zu verhindern, dass ein Farbfeld weggelassen wird. </p> </td> 
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
