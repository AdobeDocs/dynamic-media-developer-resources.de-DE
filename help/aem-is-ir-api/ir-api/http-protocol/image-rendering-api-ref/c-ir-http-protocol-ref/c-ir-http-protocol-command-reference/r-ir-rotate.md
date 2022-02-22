---
title: drehen
description: Werkstoffdrehwinkel. Definiert den Drehwinkel für Materialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# drehen{#rotate}

Werkstoffdrehwinkel. Definiert den Drehwinkel für Materialien.

` rotate= *`Winkel`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Winkel </span> </p> </td> 
  <td class="stentry"> <p>Drehwinkel in Grad (real). </p> </td> 
 </tr> 
</table>

Wiederholbare Texturmaterialien (ohne Wallpaper) um ein Vielfaches von 45° drehen, wenn sie auf flache Objekte oder Planobjekte angewendet werden.

Drehen Sie wiederholbare Texturmaterialien um beliebige Winkel, wenn sie auf Flowline- und Sketch-Objekte angewendet werden.

Drehen Sie dekale Materialien nach beliebigen Winkeln.

Positive Winkel drehen den Uhrzeigersinn. Die Textur oder die Decke wird um den Ankerpunkt gedreht ( `anchor=`); der Ankerpunkt bleibt an der Herkunft des Zielobjekts ausgerichtet.

## Eigenschaften {#section-ad4d07897ca24f63af1a4062f8618e36}

Materialattribut. Ignoriert durch feste Farbe, Tapeten, Schrank und Fensterbehandlungsmaterialien. *`angle`* Muss ein Vielfaches von 45 für wiederholbare Texturen sein, es sei denn, dies wird auf Fluss- oder Zeichenobjekte angewendet.

## Standard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, um keine Drehung durchzuführen.

## Verwandte Themen {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
