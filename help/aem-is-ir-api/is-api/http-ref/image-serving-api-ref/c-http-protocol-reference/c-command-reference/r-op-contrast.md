---
description: Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit mehr als 50 % Helligkeit erhöht und die Helligkeit von Pixeln mit weniger als 50 % Helligkeit verringert wird.
seo-description: Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit mehr als 50 % Helligkeit erhöht und die Helligkeit von Pixeln mit weniger als 50 % Helligkeit verringert wird.
seo-title: op_stroke
solution: Experience Manager
title: op_stroke
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# op_counter{#op-contrast}

Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit mehr als 50 % Helligkeit erhöht und die Helligkeit von Pixeln mit weniger als 50 % Helligkeit verringert wird.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Kontrastanpassung in Prozent (-100...100 int). </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-d319ed55057344eab0a3c93f720acdbf}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, ohne dass sich der Kontrast ändert. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Beispiel {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Verkleinern Sie den Kontrast und die Schärfe einer Bildebene mit höherer Qualität, um sie visuell an ein Hintergrundbild mit niedriger Qualität anzupassen:

... `&op_blur=3&op_contrast=-12&`

Eine zukünftige Version verwendet möglicherweise die mittlere Helligkeit des Bildes anstelle einer festen 50 % Helligkeit.
