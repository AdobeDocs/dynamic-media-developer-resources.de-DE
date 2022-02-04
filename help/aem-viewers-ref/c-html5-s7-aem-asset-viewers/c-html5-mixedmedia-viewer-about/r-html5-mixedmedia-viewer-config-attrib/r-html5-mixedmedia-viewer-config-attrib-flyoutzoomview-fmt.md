---
title: FlyoutZoomView.fmt
description: Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Wenn das angegebene Format mit <span class="codeph"> -alpha</span>, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. </p> <p>Die Komponente hat standardmäßig einen weißen Hintergrund. Um dies transparent zu machen, legen Sie daher die <span class="codeph"> background-color</span> CSS-Eigenschaft auf <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
