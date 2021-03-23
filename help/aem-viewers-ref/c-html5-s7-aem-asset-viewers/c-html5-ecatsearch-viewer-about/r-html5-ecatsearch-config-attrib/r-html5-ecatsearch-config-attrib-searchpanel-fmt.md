---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
uuid: 58b88cc9-e07a-47aa-a0d2-c81428ca4d1e
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog-Suche
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---


# SearchPanel.fmt{#searchpanel-fmt}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Image-Server verwendet. Es kann sich um ein beliebiges Format handeln, das von Image Server und dem Clientbrowser unterstützt wird. </p> <p>Wenn das angegebene Format mit <span class="codeph"> -alpha</span> endet, rendert die Komponente Bilder als transparenten Inhalt. Bei allen anderen Bildformaten behandelt die Komponente Bilder als undurchsichtig. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optional.

## Standard {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Beispiel {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
