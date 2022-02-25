---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d1f54ef2-4ed4-4fb6-9913-98bf194f9afc
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> iscommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Die Image Serving-Befehlszeichenfolge, die auf das Zoom-Bild angewendet wird. Wenn in der URL angegeben, werden alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> muss HTTP-kodiert sein als <span class="codeph"> %26</span> und <span class="codeph"> %3D</span>zurück. </p> <p> <p>Hinweis: Befehle zum Bearbeiten der Bildgröße werden nicht unterstützt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

Keine.

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

Wenn in der Viewer-URL angegeben:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wenn in den Konfigurationsdaten angegeben:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
