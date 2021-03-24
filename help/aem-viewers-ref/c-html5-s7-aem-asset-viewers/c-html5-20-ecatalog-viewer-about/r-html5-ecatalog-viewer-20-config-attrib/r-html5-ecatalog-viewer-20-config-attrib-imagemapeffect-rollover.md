---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 5%

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wann das Infofeld angezeigt werden soll. </p> <p>Wenn der Wert auf <span class="codeph"> 1</span> eingestellt ist, wird das Infofeld angezeigt, wenn die Maus in den Imagemap-Bereich eindringt (wenn die Imagemap nicht leer ist, <span class="codeph"> rollover_key</span> Attribut). </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, wird beim Klicken auf die Imagemap das Infofeld ausgelöst (wenn die Imagemap ein nicht leeres <span class="codeph"> rollover_key</span> und leere <span class="codeph"> href</span>-Attribute hat). </p> <p> Wird auf Touch-Geräten einschließlich Touch-fähigen Desktop-Systemen ignoriert und automatisch auf <span class="codeph"> 0</span> eingestellt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
