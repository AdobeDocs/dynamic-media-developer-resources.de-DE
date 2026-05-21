---
title: op_contrast
description: Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit einer Helligkeit von mehr als 50 % erhöht und die Helligkeit von Pixeln mit einer Helligkeit von weniger als 50 % reduziert wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
TQID: 'https://experienceleague.adobe.com/Ob098G38TFXX0HzB3JQOCcdD9ZnrYWrMum6XEQSmGRU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 1%

---

# op_contrast{#op-contrast}

Kontrast anpassen. Passt den Bildkontrast an, indem die Helligkeit von Pixeln mit einer Helligkeit von mehr als 50 % erhöht und die Helligkeit von Pixeln mit einer Helligkeit von weniger als 50 % reduziert wird.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Adj</span> </p> </td> 
  <td class="stentry"> <p>Kontrasteinstellung in Prozent (-100…100 int). </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-d319ed55057344eab0a3c93f720acdbf}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, für keine Kontraständerung. CMYK-Bilder oder -Ebenen werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Beispiel {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Verringern Sie den Kontrast und die Schärfe einer Bildebene mit höherer Qualität, um sie visuell an ein Hintergrundbild mit niedriger Qualität anzupassen:

… `&op_blur=3&op_contrast=-12&`

In einer zukünftigen Version wird möglicherweise die mittlere Helligkeit des Bildes anstelle einer festen Helligkeit von 50 % verwendet.
