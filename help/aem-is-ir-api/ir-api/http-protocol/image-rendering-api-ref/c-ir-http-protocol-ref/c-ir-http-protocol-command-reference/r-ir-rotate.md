---
title: drehen
description: Drehwinkel des Materials. Definiert den Drehwinkel für Materialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# drehen{#rotate}

Drehwinkel des Materials. Definiert den Drehwinkel für Materialien.

` rotate= *`Winkel`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Drehwinkel in Grad (real). </p> </td> 
 </tr> 
</table>

Drehen Sie wiederholbare Texturmaterialien (außer Tapeten) um Vielfache von 45°, wenn sie auf flache oder ebene Objekte angewendet werden.

Drehen Sie wiederholbare Texturmaterialien in beliebigen Winkeln, wenn sie auf Fließlinien- und Skizzenobjekte angewendet werden.

Drehen Sie Abziehbilder um beliebige Winkel.

Positive Winkel drehen sich im Uhrzeigersinn. Die Textur oder das Abziehbild wird um den Ankerpunkt (`anchor=`) gedreht; der Ankerpunkt bleibt auf den Ursprung des Zielobjekts ausgerichtet.

## Eigenschaften {#section-ad4d07897ca24f63af1a4062f8618e36}

Materialattribut. Wird von einfarbigen Materialien, Tapeten, Schränken und Fensterbehandlungen ignoriert. *`angle`* Wiederholbare Texturen müssen ein Vielfaches von 45 haben, es sei denn, sie werden auf Fließlinien- oder Skizzenobjekte angewendet.

## Standard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, für keine Rotation.

## Verwandte Themen {#section-f73c00e9368b478dac1fd15bb4367a12}

[Anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
