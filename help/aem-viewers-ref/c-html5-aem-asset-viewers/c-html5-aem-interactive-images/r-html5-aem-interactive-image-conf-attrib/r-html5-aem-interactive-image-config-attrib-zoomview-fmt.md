---
description: Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.
seo-description: Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
uuid: 73a2196f-0ece-497a-9a12-376dafbbae56
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Bilder
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 3%

---


# ZoomView.fmt{#zoomview-fmt}

Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. Die Komponente hat standardmäßig einen weißen Hintergrund. Um ihn transparent zu machen, setzen Sie die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
