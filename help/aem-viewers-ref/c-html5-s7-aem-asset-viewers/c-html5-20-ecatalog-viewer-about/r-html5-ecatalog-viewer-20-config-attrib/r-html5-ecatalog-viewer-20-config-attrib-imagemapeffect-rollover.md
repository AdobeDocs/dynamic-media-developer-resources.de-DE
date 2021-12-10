---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wann das Informationsfeld angezeigt werden soll. </p> <p>Wenn auf <span class="codeph"> 1</span>, wird das Infofeld angezeigt, wenn die Maus den Imagemap-Bereich betritt (falls die Imagemap nicht leer ist). <span class="codeph"> rollover_key</span> -Attribut). </p> <p>Wenn auf <span class="codeph"> 0</span> Infofeld wird ausgelöst, wenn die Imagemap ausgewählt wird (wenn die Imagemap nicht leer ist) <span class="codeph"> rollover_key</span> und leer <span class="codeph"> href</span> -Attribute). </p> <p> Wird auf Touch-Geräten, einschließlich Touch-optimierter Desktop-Systeme, ignoriert und automatisch auf <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
