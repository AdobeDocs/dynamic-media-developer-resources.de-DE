---
description: Werkstoffdrehwinkel Definiert den Drehwinkel für Materialien.
seo-description: Werkstoffdrehwinkel Definiert den Drehwinkel für Materialien.
seo-title: drehen
solution: Experience Manager
title: drehen
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 7%

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
