---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Legen Sie fest auf <span class="codeph"> 1</span> , um das Vorabladen des gezoomten Bildes zu aktivieren, oder auf <span class="codeph"> 0</span> , um das Zoombild nach Bedarf schrittweise zu laden. </p> <p> <p>Hinweis: Wenn Sie diese Option aktivieren, kann dies zu einer wesentlich höheren Bandbreitennutzung führen. Das gezoomte Bild wird vollständig geladen, auch wenn der Benutzer keine Zoom-Aktion auslöst. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
