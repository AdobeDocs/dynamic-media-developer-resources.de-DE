---
title: op_contrast
description: Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit mehr als 50 % Helligkeit erhöht und die Helligkeit von Pixeln mit weniger als 50 % Helligkeit verringert wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# op_contrast{#op-contrast}

Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit mehr als 50 % Helligkeit erhöht und die Helligkeit von Pixeln mit weniger als 50 % Helligkeit verringert wird.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Kontrastanpassung in Prozent (-100...100 int). </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-d319ed55057344eab0a3c93f720acdbf}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp` Wird von Effektebenen ignoriert.

## Standard {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, ohne Kontraständerung. CMYK-Bilder oder -Ebenen werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Beispiel {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Verringern Sie den Kontrast und die Schärfe einer höheren Bildschicht, um sie visuell an ein Hintergrundbild mit niedriger Qualität anzupassen:

... `&op_blur=3&op_contrast=-12&`

In einer künftigen Version wird möglicherweise die mittlere Helligkeit des Bildes anstelle einer fixierten 50-%-Helligkeit verwendet.
