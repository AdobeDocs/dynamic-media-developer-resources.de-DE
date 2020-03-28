---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 1ed18115-9e29-434a-a48d-40bf6b48fe6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet werden soll. Wenn das angegebene Format mit <span class="codeph"> "-alpha"</span>endet, rendert die Komponente die Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. Beachten Sie, dass die Komponente standardmäßig einen weißen Hintergrund hat. Um eine vollständige Transparenz zu gewährleisten, legen Sie daher die <span class="codeph"> CSS-Eigenschaft "background-color</span> "auf <span class="codeph"> transparent</span>fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
