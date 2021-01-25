---
description: Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildabweichungen oder Zuschneidungsparameter, die auf die Größe des Bildes normalisiert werden.
seo-description: Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildabweichungen oder Zuschneidungsparameter, die auf die Größe des Bildes normalisiert werden.
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# coordN{#coordn}

Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildabweichungen oder Zuschneidungsparameter, die auf die Größe des Bildes normalisiert werden.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>Koordinatenoffset normalisiert auf Bildgröße (real, real) </p></td> 
 </tr> 
</table>

Positive Werte bewegen sich nach unten rechts.

In vielen Fällen ist die Referenzposition der Mittelpunkt des Bilds. In diesem Fall entspricht 0,0 der Bildmitte, -0,5, -0,5 der oberen linken Ecke und 0,5,0,5 der unteren rechten Ecke.

Wird auch verwendet, um Bildgrößen oder Rechteckgrößen relativ zur Größe der Ebene 0 anzugeben. In diesem Fall müssen die Werte größer als 0 sein. 0 kann angeben, dass ein bestimmter Standardwert verwendet werden soll. 1,1 gibt eine Größe an, die der Ebene 0 entspricht.
