---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Viewer,SDK/API,Inline-Zoom
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet werden soll. Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. </p> <p>Beachten Sie, dass die Komponente standardmäßig einen weißen Hintergrund hat. Um dies vollständig transparent zu machen, setzen Sie daher die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
