---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: CallToAction.fmt
solution: Experience Manager
title: CallToAction.fmt
topic: Dynamic media
uuid: c85160e2-431f-42af-a468-c754bfe86ecd
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---


# CallToAction.fmt{#calltoaction-fmt}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. </p> <p>Wenn das angegebene Format mit "<span class="codeph"> -alpha</span>"endet, rendert die Komponente die Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente die Bilder als undurchsichtig. </p> </td> 
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

