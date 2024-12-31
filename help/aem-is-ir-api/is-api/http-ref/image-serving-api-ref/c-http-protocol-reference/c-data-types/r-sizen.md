---
description: Normalisierte Größe. Wird verwendet, um Bildgrößen oder Rechteckgrößen anzugeben, die relativ zur Größe von Ebene 0 oder einem anderen Bild normalisiert sind.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# sizeN{#sizen}

Normalisierte Größe. Wird verwendet, um Bildgrößen oder Rechteckgrößen anzugeben, die relativ zur Größe von Ebene 0 oder einem anderen Bild normalisiert sind.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> NX</span> </span>, <span class="codeph"><span class="varname"> NY</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> NX</span> </span>, <span class="codeph"><span class="varname"> NY</span></span> </p></td> 
  <td class="stentry"> <p>Normalisierte Breite und Höhe relativ zu einem anderen Bild (real, real, größer als 0) </p></td> 
 </tr> 
</table>

Sowohl *nx* als auch *ny* müssen größer als 0 sein. 0,0 kann bedeuten, dass eine bestimmte Standardgröße verwendet werden soll. 1,1 legt eine Größe fest, die der Größe des Referenzbilds entspricht.
