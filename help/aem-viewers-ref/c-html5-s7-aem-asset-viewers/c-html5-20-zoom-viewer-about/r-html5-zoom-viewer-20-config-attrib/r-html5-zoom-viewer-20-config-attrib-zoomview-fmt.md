---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
feature: Dynamic Media Classic, Viewer, SDK/API, Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. Die Komponente hat standardmäßig einen weißen Hintergrund. Um ihn transparent zu machen, setzen Sie die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
