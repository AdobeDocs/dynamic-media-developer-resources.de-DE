---
description: Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird.
seo-description: Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
uuid: be3d49d1-d5d2-4ecd-bc8f-fe5f80204c76
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog-Suche
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26</span> bzw. <span class="codeph"> %3D</span> HTTP-kodiert sein. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Wenn in der Viewer-URL angegeben.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Wenn in den Konfigurationsdaten angegeben.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
