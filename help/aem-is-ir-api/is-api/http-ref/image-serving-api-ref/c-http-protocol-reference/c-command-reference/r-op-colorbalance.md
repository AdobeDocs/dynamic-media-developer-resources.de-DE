---
description: Passen Sie den Farbbalance an. Passt den Wert jeder RGB-Farbkomponente separat an.
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# op_colorbalance{#op-colorbalance}

Passen Sie den Farbbalance an. Passt den Wert jeder RGB-Farbkomponente separat an.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Anpassung roter Komponenten (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Anpassung grüner Komponenten (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Blaue Komponentenanpassung (-100...+100 int). </p></td> 
 </tr> 
</table>

Graue und CMYK-Eingabebilddaten werden mithilfe einer naiven Konvertierung in RGB konvertiert, die bei aktiviertem Farbmanagement nicht präzise ist.

## Eigenschaften {#section-dff9c934f7c1442bbd02379b688d82e2}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp` Wird von Effektebenen ignoriert. CMYK-Bilder und -Ebenen werden vor der Anwendung des Vorgangs in RGB konvertiert.

## Standard {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` für keine Farbänderung.

## Beispiel {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Push the color balance to red:

... `&op_colorBalance=100,0,0&`...
