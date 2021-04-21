---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Die Image Serving-Befehlszeichenfolge, die auf das Zoombild angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26</span> bzw. <span class="codeph"> %3D</span> HTTP-kodiert sein. </p> <p> <p>Hinweis:  Bildgrößenbearbeitungsbefehle werden nicht unterstützt. </p> </p> </td> 
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

Bei Angabe in den Konfigurationsdaten:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
