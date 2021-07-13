---
description: Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildabweichungen oder Zuschnittparameter, die auf die Bildgröße normalisiert sind.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# coordN{#coordn}

Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildabweichungen oder Zuschnittparameter, die auf die Bildgröße normalisiert sind.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>Koordinatenversatz, der auf die Bildgröße normalisiert wird (real, real) </p></td> 
 </tr> 
</table>

Positive Werte bewegen sich nach unten rechts.

In vielen Fällen ist die Referenzposition der Mittelpunkt des Bildes. In diesem Fall entspricht 0,0 der Bildmitte, -0,5, -0,5 der oberen linken Ecke und 0,5,0,5 der unteren rechten Ecke.

Wird auch verwendet, um Bildgrößen oder Rechteckgrößen im Verhältnis zur Größe der Ebene 0 anzugeben. In diesem Fall müssen die Werte größer als 0 sein. 0 kann angeben, dass ein bestimmter Standardwert verwendet werden soll. 1,1 gibt eine Größe an, die der Ebene 0 entspricht.
