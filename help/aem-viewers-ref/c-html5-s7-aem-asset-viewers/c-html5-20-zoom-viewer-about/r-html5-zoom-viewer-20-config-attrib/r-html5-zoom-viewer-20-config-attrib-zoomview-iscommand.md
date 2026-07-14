---
title: ZoomView.isCommand
description: ZoomView.isCommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bab0a648-a365-4df1-bded-ba0202e62e1f
TQID: 'https://experienceleague.adobe.com/rDroGBV5rSLT3BwcuTs9mfz8Tp00lJf2oBqV63DlWOs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 6%

---

# ZoomView.isCommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> IsCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Die Befehlszeichenfolge für die Bildbereitstellung, die auf das Zoom-Bild angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26 bzw</span> <span class="codeph"> %3D</span> HTTP-codiert sein. </p> <p> <p>Hinweis: Befehle zur Bearbeitung der Bildgröße werden nicht unterstützt. </p> </p> </td> 
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

