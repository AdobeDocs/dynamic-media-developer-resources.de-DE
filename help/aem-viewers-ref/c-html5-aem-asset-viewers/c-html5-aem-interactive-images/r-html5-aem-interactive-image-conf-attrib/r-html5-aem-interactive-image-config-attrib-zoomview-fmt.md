---
title: ZoomView.fmt
description: Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a023abb-71c7-4db5-8d05-bf0a4b1fc3a0
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# ZoomView.fmt{#zoomview-fmt}

Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. Die Komponente hat standardmäßig einen weißen Hintergrund. Um dies transparent zu machen, setzen Sie daher die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
