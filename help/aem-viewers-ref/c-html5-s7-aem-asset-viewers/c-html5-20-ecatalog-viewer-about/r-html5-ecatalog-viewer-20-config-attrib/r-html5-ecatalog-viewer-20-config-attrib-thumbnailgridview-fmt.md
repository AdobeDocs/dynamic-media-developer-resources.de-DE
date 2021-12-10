---
title: ThumbnailGridView.fmt
description: ThumbnailGridView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 916ee5d1-e398-4923-9107-96f649033298
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---

# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. Es kann sich um einen beliebigen Wert handeln, den Image Server und der Client-Browser unterstützen. Wenn das angegebene Format mit <span class="codeph"> -alpha</span>, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

Optional.

## Standard {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## Beispiel {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`
