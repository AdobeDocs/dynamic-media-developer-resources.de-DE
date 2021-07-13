---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a713b8f1-e834-457d-b038-eb30b25f905f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# SearchPanel.fmt{#searchpanel-fmt}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. Es kann sich um ein beliebiges Format handeln, das vom Image-Server und vom Client-Browser unterstützt wird. </p> <p>Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als deckend. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optional.

## Standard {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Beispiel {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
