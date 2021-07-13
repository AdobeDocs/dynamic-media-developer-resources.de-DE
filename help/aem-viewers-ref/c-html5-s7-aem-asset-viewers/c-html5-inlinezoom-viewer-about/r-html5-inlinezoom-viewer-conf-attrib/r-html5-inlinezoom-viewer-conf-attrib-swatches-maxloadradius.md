---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Viewer,SDK/API,Inline-Zoom
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Verhalten beim Vorausfüllen der Komponente an. Wenn auf <span class="codeph"> -1</span> gesetzt, werden alle Muster gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. Wenn auf <span class="codeph"> 0</span> gesetzt, werden nur sichtbare Farbfelder geladen. </p> <p><span class="codeph"> <span class="varname"> </span></span> preloadnbraries definiert, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
