---
title: ZoomView.isCommand
description: ZoomView.isCommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: faa6344a-a0b5-4b27-818b-81e9e0b721b4
TQID: 'https://experienceleague.adobe.com/XO1YCckMogWh-NmUUI4Pj7x1iHWHCF6x5W-GLZR2tI0'
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
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> IsCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Die Befehlszeichenfolge für die Bildbereitstellung, die auf das Zoom-Bild angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26 bzw</span> <span class="codeph"> %3D</span> HTTP-codiert sein. </p> <p> <p>Hinweis: Befehle zur Bearbeitung der Bildgröße werden nicht unterstützt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Keine.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Wenn in der Viewer-URL angegeben:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wenn in den Konfigurationsdaten angegeben:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
