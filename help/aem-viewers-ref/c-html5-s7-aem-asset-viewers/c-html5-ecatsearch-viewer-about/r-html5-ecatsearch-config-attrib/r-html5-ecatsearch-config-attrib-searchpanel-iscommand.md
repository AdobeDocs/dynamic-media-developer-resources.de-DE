---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
topic: Dynamic Media
uuid: 7496fea1-8a69-4749-ab4b-ae6d375441b8
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 10%

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Die Image Serving-Befehlszeichenfolge, die auf alle Miniaturansichten angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26</span> bzw. <span class="codeph"> %3D</span> HTTP-kodiert sein. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-df5a0604766b4ac2b9a6742b377e427c}

Optional.

## Standard {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Keine.

## Beispiel {#section-813de2905d6c44c0991cfe0931581462}

Wenn in der Viewer-URL angegeben.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Wenn in den Konfigurationsdaten angegeben.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
