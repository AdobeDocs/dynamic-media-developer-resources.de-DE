---
description: 'null'
seo-description: 'null'
seo-title: Muster.fmt
solution: Experience Manager
title: Muster.fmt
topic: Dynamic media
uuid: 61e6372c-bab9-4aac-a8a1-dffecc2e4903
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Muster.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. Wenn das angegebene Format mit <span class="codeph"> -alpha</span>endet, rendert die Komponente die Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. Beachten Sie, dass die Komponente standardmäßig einen weißen Hintergrund hat. Um den Hintergrund transparent zu machen, legen Sie daher die CSS-Eigenschaft " <span class="codeph"> background-color</span> "auf <span class="codeph"> transparent</span>fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
