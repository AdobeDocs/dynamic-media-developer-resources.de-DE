---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wann das Informationsfeld angezeigt werden soll. </p> <p>Wenn der Wert auf <span class="codeph"> 1</span> festgelegt ist, wird das Infofeld angezeigt, wenn die Maus in den Imagemap-Bereich gelangt (falls die Imagemap ein nicht leeres Attribut aufweist, das Attribut <span class="codeph"> rollover_key</span> ). </p> <p>Wenn der Wert auf "<span class="codeph"> 0</span>" gesetzt ist, wird das Infofeld ausgelöst, wenn die Imagemap ausgewählt wird (wenn die Imagemap nicht leere Attribute "<span class="codeph"> rollover_key</span>"und "<span class="codeph"> href</span>" aufweist). </p> <p> Wird auf Touch-Geräten, einschließlich Touch-optimierter Desktop-Systeme, ignoriert und automatisch auf <span class="codeph"> 0</span> gesetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
