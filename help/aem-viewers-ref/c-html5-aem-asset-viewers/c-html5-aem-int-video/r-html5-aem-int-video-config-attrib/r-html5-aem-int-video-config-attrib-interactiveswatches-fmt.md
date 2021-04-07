---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: InteractiveSwatches.fmt
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. </p> <p>Wenn das angegebene Format mit "<span class="codeph"> -alpha</span>"endet, rendert die Komponente die Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente die Bilder als undurchsichtig. Beachten Sie, dass die Komponente standardmäßig einen weißen Hintergrund hat. Um die Transparenz zu gewährleisten, setzen Sie daher die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
