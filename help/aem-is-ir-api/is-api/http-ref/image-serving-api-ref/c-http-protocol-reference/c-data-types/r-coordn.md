---
title: coordN
description: Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildversätze oder Zuschnittparameter, die auf die Bildgröße normalisiert wurden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# coordN{#coordn}

Normalisierte Koordinaten. Wird verwendet, um relative Positionen innerhalb eines Bildes anzugeben, z. B. Bildversätze oder Zuschnittparameter, die auf die Bildgröße normalisiert wurden.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> NX</span> </span>, <span class="codeph"><span class="varname"> NY</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> NX</span> </span>, <span class="codeph"><span class="varname"> NY</span></span> </p></td> 
  <td class="stentry"> <p>Koordinatenversatz, der auf die Größe eines Bildes normalisiert ist (real, real) </p></td> 
 </tr> 
</table>

Positive Werte werden nach unten rechts verschoben.

Häufig ist die Referenzposition der Mittelpunkt des Bildes. In diesem Fall entspricht `0,0` der Bildmitte, `-0.5,-0.5` der linken oberen Ecke und `0.5,0.5` der rechten unteren Ecke.

Sie wird auch verwendet, um die Bildgröße oder Rechteckgröße relativ zur Größe der Ebene 0 anzugeben. In diesem Fall muss der Wert größer als 0 sein. 0 gibt an, dass ein bestimmter Standardwert verwendet werden soll. Der Wert `1,1` gibt eine Größe an, die der Größe der Ebene 0 entspricht.
