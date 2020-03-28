---
description: Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird.
seo-description: Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
topic: Dynamic media
uuid: 59a25b65-a08f-46e9-a9eb-33672e4a0cb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesView.iscommand{#favoritesview-iscommand}

Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> HTTP-kodiert als <span class="codeph"> %26</span> bzw. <span class="codeph"> %3D</span>sein. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Wenn in der Viewer-URL angegeben.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wenn in den Konfigurationsdaten angegeben.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
