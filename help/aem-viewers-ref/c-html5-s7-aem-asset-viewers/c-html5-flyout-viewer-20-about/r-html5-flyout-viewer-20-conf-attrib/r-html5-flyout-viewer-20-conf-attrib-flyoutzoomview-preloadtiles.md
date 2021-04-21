---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Setzen Sie diese Einstellung auf <span class="codeph"> 1</span>, um das Vorladen des gezoomten Bildes zu aktivieren, oder setzen Sie sie auf <span class="codeph"> 0</span>, um das Zoombild nach Bedarf inkrementell zu laden. </p> <p> <p>Hinweis:  Wenn Sie diese Option aktivieren, kann dies zu einer wesentlich höheren Bandbreitennutzung führen. Das gezoomte Bild wird vollständig geladen, auch wenn der Benutzer keine Zoomaktion auslöst. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
