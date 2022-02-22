---
description: Renderausrichtung der Textur. Gibt an, welche der vom ausgewählten Vignettenobjekt definierten Ausgangspunkte verwendet werden sollen.
solution: Experience Manager
title: align
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 4%

---

# align {#align}

Renderausrichtung der Textur. Gibt an, welche der vom ausgewählten Vignettenobjekt definierten Ausgangspunkte verwendet werden sollen.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Standardursprung (zentrierte Übereinstimmung). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Kontinuierliche Übereinstimmungsursache. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Zufällige Ausrichtung. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>Benutzerdefinierte Herkunft. </p></td> 
 </tr> 
</table>

Der Renderer wendet die Textur auf das Objekt an, sodass der Texturankerpunkt ( `anchor=`) entspricht dem angegebenen Ausgangspunkt.

Jedes Objekt kann bis zu sechs Ausgangspunkte definieren (0, 1, 3, 4, 5, 6). Wenn eine `align` -Wert angegeben ist, der entsprechende Ausgangspunkt jedoch nicht durch das Vignettenobjekt definiert ist, wird der standardmäßige Ausgangspunkt (Zentrieren-Übereinstimmung) verwendet.

`align=2` Gibt eine zufällige Texturausrichtung an. In diesem Fall `anchor=` wird effektiv ignoriert.

Hauptsächlich für Polstermaterialien, möglicherweise für Bekleidungsstoffe, verwendet, um die Ausrichtung der Textur zwischen benachbarten Objekten zu verwalten.

## Eigenschaften {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materialattribut. Wird ignoriert, wenn ein Rahmen-Objekt für Wand-, Schrank-, Geräte- oder Fensterverkleidungen ausgewählt ist oder wenn das Material keine wiederholbare Textur ist.

## Standard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, wenn das Material auf einem Katalogeintrag basiert, andernfalls 0 (zentriert).

## Verwandte Themen {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
