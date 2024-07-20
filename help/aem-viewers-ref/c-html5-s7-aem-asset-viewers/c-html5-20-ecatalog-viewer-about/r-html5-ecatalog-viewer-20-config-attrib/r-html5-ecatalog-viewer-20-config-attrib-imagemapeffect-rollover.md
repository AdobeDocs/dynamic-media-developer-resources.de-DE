---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wann das Informationsfeld angezeigt werden soll. </p> <p>Wenn der Wert auf <span class="codeph"> 1</span> festgelegt ist, wird das Infofeld angezeigt, wenn die Maus in den Imagemap-Bereich gelangt (falls die Imagemap nicht leer ist, Attribut <span class="codeph"> rollover_key</span> ). </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, wird das Infofeld ausgelöst, wenn die Imagemap ausgewählt wird (wenn die Imagemap nicht leere Attribute <span class="codeph"> rollover_key</span> und leere Attribute <span class="codeph"> href</span> aufweist). </p> <p> Wird auf Touch-Geräten, einschließlich Touch-optimierter Desktop-Systeme, ignoriert und automatisch auf <span class="codeph"> 0</span> gesetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
