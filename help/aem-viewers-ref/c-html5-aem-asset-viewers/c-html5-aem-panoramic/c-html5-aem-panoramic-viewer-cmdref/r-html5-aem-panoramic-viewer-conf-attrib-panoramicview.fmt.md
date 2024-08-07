---
title: PanoramicView.fmt
description: Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet wird. Wenn das angegebene Format mit &quot;-alpha&quot;endet, rendert die Komponente die Bilder als transparent. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. Die Komponente hat standardmäßig einen transparenten Hintergrund. Um es undurchsichtig zu machen, setzen Sie daher die CSS-Eigenschaft `background-color` auf `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet werden soll. Wenn das angegebene Format mit "-alpha"endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. Die Komponente hat standardmäßig einen transparenten Hintergrund. Um die CSS-Eigenschaft für die Hintergrundfarbe zu deckeln, legen Sie daher die gewünschte Farbe fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
