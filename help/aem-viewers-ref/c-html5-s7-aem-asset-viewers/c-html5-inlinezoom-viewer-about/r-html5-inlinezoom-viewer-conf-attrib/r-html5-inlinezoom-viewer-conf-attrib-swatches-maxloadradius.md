---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 5%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadNbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Verhalten beim Vorausfüllen der Komponente an. Wenn auf <span class="codeph"> -1 festgelegt</span> werden alle Farbfelder gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. Wenn auf <span class="codeph"> 0 festgelegt</span> werden nur sichtbare Farbfelder geladen. </p> <p><span class="codeph"> <span class="varname"> preloadNbr</span></span> legt fest, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
