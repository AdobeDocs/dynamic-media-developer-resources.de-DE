---
title: op_colorbalance
description: Farbausgleich anpassen. Passt den Wert der einzelnen RGB-Farbkomponenten separat an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

Farbausgleich anpassen. Passt den Wert der einzelnen RGB-Farbkomponenten separat an.

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Rote Komponenteneinstellung (-100…+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Grüne Komponenteneinstellung (-100…+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Blaue Komponenteneinstellung (-100…+100 int). </p></td> 
 </tr> 
</table>

Graue und CMYK-Eingabebilddaten werden mithilfe der naiven Konvertierung in RGB konvertiert, was bei aktiviertem Farbmanagement nicht genau ist.

## Eigenschaften {#section-dff9c934f7c1442bbd02379b688d82e2}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert. CMYK-Bilder und -Ebenen werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Standard {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` für keine Änderung der Farben.

## Beispiel {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Drücken Sie den Farbabgleich in Richtung Rot:

… `&op_colorBalance=100,0,0&`…
