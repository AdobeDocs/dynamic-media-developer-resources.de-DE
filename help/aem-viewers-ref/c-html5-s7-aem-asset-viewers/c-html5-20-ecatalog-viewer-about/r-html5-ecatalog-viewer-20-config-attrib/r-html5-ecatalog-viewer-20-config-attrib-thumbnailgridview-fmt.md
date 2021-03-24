---
description: ThumbnailGridView.fmt
solution: Experience Manager
title: ThumbnailGridView.fmt
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. Es kann sich um einen beliebigen Wert handeln, den Image Server und der Client-Browser unterstützen. Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

Optional.

## Standard {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## Beispiel {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`
