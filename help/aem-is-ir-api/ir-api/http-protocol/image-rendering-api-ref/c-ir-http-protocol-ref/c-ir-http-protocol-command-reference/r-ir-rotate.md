---
description: Werkstoffdrehwinkel Definiert den Drehwinkel für Materialien.
solution: Experience Manager
title: drehen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 6%

---


# rotate{#rotate}

Werkstoffdrehwinkel Definiert den Drehwinkel für Materialien.

` rotate= *`Winkel`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Winkel </span> </p> </td> 
  <td class="stentry"> <p>Drehwinkel in Grad (real). </p> </td> 
 </tr> 
</table>

Drehen Sie wiederholbare Texturmaterialien (ohne Wallpaper) um ein Vielfaches von 45 Grad, wenn sie auf flache Objekte oder Plane Objekte angewendet werden.

Drehen Sie wiederholbare Texturmaterialien mit beliebigen Winkeln, wenn sie auf Flusslinien- und Sketch-Objekte angewendet werden.

Drehen Sie dekale Materialien nach beliebigen Winkeln.

Positive Winkel drehen im Uhrzeigersinn. Die Textur oder der Dekorationspunkt wird um den Ankerpunkt ( `anchor=`) gedreht. Der Verankerungspunkt bleibt an der Herkunft des Zielgruppe-Objekts ausgerichtet.

## Eigenschaften {#section-ad4d07897ca24f63af1a4062f8618e36}

Materialattribut. Eingebettet in einfarbige Materialien, Tapeten, Schränke und Fensterbehandlungen. *`angle`* muss ein Vielfaches von 45 für wiederholbare Texturen sein, es sei denn, sie werden auf Textlinien- oder Skizzierobjekte angewendet.

## Standard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, ohne Drehung.

## Verwandte Themen {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
