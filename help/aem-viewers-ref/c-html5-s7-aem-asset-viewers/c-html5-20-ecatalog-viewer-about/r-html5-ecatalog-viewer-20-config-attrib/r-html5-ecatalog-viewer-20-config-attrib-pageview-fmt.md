---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 5432393e265fba888579d700cf2f414dc4f680af
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Bildserver verwendet. Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Für alle anderen Bildformate behandelt die Komponente Bilder als undurchsichtig. Die Komponente hat standardmäßig einen weißen Hintergrund. Um sie transparent zu gestalten, legen Sie daher die <span class="codeph"> background-color</span> CSS-Eigenschaft auf <span class="codeph"> transparent fest</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optional.

## Standard {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Beispiel {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
