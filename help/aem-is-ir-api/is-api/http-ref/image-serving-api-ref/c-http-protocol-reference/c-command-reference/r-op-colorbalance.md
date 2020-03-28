---
description: Passen Sie den Farbbalance an. Passt den Wert jeder RGB-Farbkomponente separat an.
seo-description: Passen Sie den Farbbalance an. Passt den Wert jeder RGB-Farbkomponente separat an.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Scene7 Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_colorbalance{#op-colorbalance}

Passen Sie den Farbbalance an. Passt den Wert jeder RGB-Farbkomponente separat an.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Rote Komponentenanpassung (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Grüne Komponentenanpassung (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Blaue Komponentenanpassung (-100...+100 int). </p></td> 
 </tr> 
</table>

Grau- und CMYK-Eingabebilddaten werden mithilfe einer naiven Konvertierung in RGB konvertiert, die bei aktiviertem Farbmanagement nicht exakt ist.

## Eigenschaften {#section-dff9c934f7c1442bbd02379b688d82e2}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, falls `layer=comp`dies der Fall ist. Von Effektebenen ignoriert. CMYK-Bilder und -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Standard {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` für keine Farbänderung.

## Beispiel {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Pushen Sie den Farbbalance in Richtung Rot:

… `&op_colorBalance=100,0,0&`…
