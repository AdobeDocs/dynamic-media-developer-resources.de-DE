---
title: ImageMapEffect.mode
description: ImageMapEffect.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 86a3f04f-6593-4778-a8a4-1ec19800ceeb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# ImageMapEffect.mode{#imagemapeffect-mode}

`[ImageMapEffect.|<containerId>_imageMapEffect.]mode=icon|region|auto|none`

<table id="table_4A3D7D66D76A403199303155318D0DE1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">|Region|Auto|Keine </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Darstellung der Imagemap an. </p> <p> 
     <ul id="ul_DDA49C152718486E853213E6FC2182B2"> 
      <li id="li_18F86AB4D2F544319CCDF7BE376ABA53"> <p> <span class="codeph"> Symbol- </span> Zuordnungssymbole werden statisch auf dem Desktop und auf Touch-Geräten angezeigt. </p> </li> 
      <li id="li_F8832681CDD6456E9147A37C99BAFFED"> <p> <span class="codeph"> Bereich </span> rendert Imagemap-Bereiche. Auf dem Desktop werden sie beim Rollover angezeigt und auf Touch-Geräten sind sie immer sichtbar. </p> </li> 
      <li id="li_9F7DD686E8104AEB944505363F433C0F"> <p> <span class="codeph"> der automatischen </span> auf Desktop-Systemen werden Imagemap-Bereiche beim Rollover angezeigt und auf Touch-Geräten sind immer Zuordnungssymbole sichtbar. </p> </li> 
      <li id="li_7CB644F3A029480293B46F44FF8D03B6"> <p> <span class="codeph"> None deaktiviert </span> Imagemaps. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-6d3a96988a074a73a71b6ebd0524f272}

Optional.

## Standard {#section-64fdf33e0f874edaad5a9bcf7ab58dc7}

`icon`

## Beispiel {#section-319450f834e5406fb1bca77372e03b4b}

`mode=auto`
