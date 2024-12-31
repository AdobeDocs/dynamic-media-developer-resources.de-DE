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
   <td colname="col2"> <p>Gibt an, wann das Infobedienfeld angezeigt werden soll. </p> <p>Wenn auf <span class="codeph"> 1</span> festgelegt, wird das Infobedienfeld angezeigt, wenn die Maus in den Imagemap-Bereich eintritt (falls die Imagemap ein nicht leeres, <span class="codeph"> rollover_key</span>-Attribut aufweist). </p> <p>Wenn auf <span class="codeph"> 0</span> festgelegt, wird das Infobedienfeld ausgelöst, wenn die Imagemap ausgewählt wird (wenn die Imagemap einen nicht leeren <span class="codeph">-Rollover-Schlüssel </span> leere <span class="codeph"> href</span>-Attribute aufweist). </p> <p> Wird auf Touch-Geräten ignoriert, einschließlich Touch-optimierter Desktop-Systeme, und wird automatisch auf <span class="codeph"> 0</span> gesetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Beispiel {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
