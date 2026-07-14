---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
TQID: 'https://experienceleague.adobe.com/V5KPk6tOhMcCUtL7iraaeBNt4xp81Uo7FTpT-1Z44ks'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 5%

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

