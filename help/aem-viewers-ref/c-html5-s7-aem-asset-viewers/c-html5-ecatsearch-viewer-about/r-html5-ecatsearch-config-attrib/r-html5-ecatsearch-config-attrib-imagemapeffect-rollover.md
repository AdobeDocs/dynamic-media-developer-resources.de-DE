---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wann das Informationsfeld angezeigt werden soll. </p> <p>Wenn auf <span class="codeph"> 1</span> gesetzt, wird das Infofeld angezeigt, wenn die Maus in den Imagemap-Bereich gelangt (falls die Imagemap nicht leer ist, Attribut <span class="codeph"> rollover_key</span> ). </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, wird das Infofeld beim Klicken auf die Imagemap ausgelöst (wenn die Imagemap nicht leere <span class="codeph"> Rollover_key</span> und leere <span class="codeph"> href</span> Attribute aufweist). </p> <p> Wird auf Touch-Geräten, einschließlich Touch-optimierter Desktop-Systeme, ignoriert und automatisch auf <span class="codeph"> 0</span> gesetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
