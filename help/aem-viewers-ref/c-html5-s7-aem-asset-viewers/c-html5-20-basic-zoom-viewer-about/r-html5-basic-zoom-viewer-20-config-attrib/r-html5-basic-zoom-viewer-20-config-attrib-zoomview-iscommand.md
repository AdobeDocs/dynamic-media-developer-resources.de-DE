---
title: ZoomView.isCommand
description: ZoomView.isCommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d1f54ef2-4ed4-4fb6-9913-98bf194f9afc
TQID: 'https://experienceleague.adobe.com/-ZvWDwC7i5fQbTzDKxdF3f5xu8r59TT-3P2suXlcjDg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 6%

---

# ZoomView.isCommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> IsCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Die Befehlszeichenfolge für die Bildbereitstellung, die auf das Zoom-Bild angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26 bzw</span> <span class="codeph"> %3D</span> HTTP-codiert sein. </p> <p> <p>Hinweis: Befehle zur Bearbeitung der Bildgröße werden nicht unterstützt. </p> </p> </td> 
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
