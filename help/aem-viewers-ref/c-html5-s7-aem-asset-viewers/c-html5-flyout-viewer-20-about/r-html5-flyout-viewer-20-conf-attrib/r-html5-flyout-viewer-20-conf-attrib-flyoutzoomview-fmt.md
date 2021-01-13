---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 1ed18115-9e29-434a-a48d-40bf6b48fe6f
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet werden soll. Wenn das angegebene Format mit <span class="codeph"> "-alpha"</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. Beachten Sie, dass die Komponente standardmäßig einen weißen Hintergrund hat. Um die Transparenz zu gewährleisten, setzen Sie daher die CSS-Eigenschaft <span class="codeph"> background-color</span> auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
