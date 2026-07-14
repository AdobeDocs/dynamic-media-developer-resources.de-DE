---
description: SearchPanel.isCommand
solution: Experience Manager
title: SearchPanel.isCommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
TQID: 'https://experienceleague.adobe.com/oVEwukbSyBWx9uiIEYajmMTBJcy4WsqBOx8v4d7f24E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 51
ht-degree: 7%

---

# SearchPanel.isCommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Die Image-Serving-Befehlszeichenfolge, die auf alle Miniaturen angewendet wird. Wenn in der URL angegeben, müssen alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26 bzw</span> <span class="codeph"> %3D</span> HTTP-codiert sein. </p> </td> 
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

