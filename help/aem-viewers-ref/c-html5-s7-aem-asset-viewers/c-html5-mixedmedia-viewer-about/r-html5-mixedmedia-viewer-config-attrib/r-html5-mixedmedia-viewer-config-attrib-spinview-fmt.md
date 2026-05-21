---
title: SpinView.fmt
description: SpinView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4bb6c242-9f1a-440f-9fca-bf26e66e4114
TQID: 'https://experienceleague.adobe.com/eA-uGFDYcP8zvLRFVkqPw-57sRd-NGV0Kw-2IcrDMn8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 4%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_68C0C3D5C60640DC9A8EE04EA685AB99"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Bildserver verwendet. Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Für alle anderen Bildformate behandelt die Komponente Bilder als undurchsichtig. </p> <p>Die Komponente hat standardmäßig einen weißen Hintergrund. Um sie transparent zu gestalten, legen Sie daher die <span class="codeph"> background-color</span> CSS-Eigenschaft auf <span class="codeph"> transparent fest</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
