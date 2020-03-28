---
description: 'null'
seo-description: 'null'
seo-title: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
topic: Dynamic media
uuid: 276122d8-2109-42eb-be13-bead35cd3fe2
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wann das Infofeld angezeigt werden soll. </p> <p>Bei Einstellung auf <span class="codeph"> 1</span>wird das Infofeld angezeigt, wenn die Maus in den Imagemap-Bereich gelangt (falls die Imagemap nicht leer ist, <span class="codeph"> rollover_key</span> -Attribut). </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> eingestellt ist, wird beim Klicken auf die Imagemap das Infofeld ausgelöst (wenn die Imagemap über einen nicht leeren <span class="codeph"> rollover_key</span> -Wert und leere <span class="codeph"> href</span> -Attribute verfügt). </p> <p> Wird auf Touch-Geräten einschließlich Touch-fähigen Desktop-Systemen ignoriert und automatisch auf <span class="codeph"> 0</span>eingestellt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
