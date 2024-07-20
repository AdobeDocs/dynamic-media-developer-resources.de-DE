---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bab0a648-a365-4df1-bded-ba0202e62e1f
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Die Image Serving-Befehlszeichenfolge, die auf das Zoom-Bild angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> HTTP-kodiert sein als <span class="codeph"> %26</span> bzw. <span class="codeph"> %3D</span>. </p> <p> <p>Hinweis: Befehle zum Bearbeiten der Bildgröße werden nicht unterstützt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

Keine.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

Wenn in der Viewer-URL angegeben:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wenn in den Konfigurationsdaten angegeben:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
