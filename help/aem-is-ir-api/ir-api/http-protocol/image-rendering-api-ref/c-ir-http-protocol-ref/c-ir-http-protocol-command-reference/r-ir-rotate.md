---
title: drehen
description: Drehwinkel des Materials. Definiert den Drehwinkel für Materialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
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

Materialattribut. Wird von einfarbigen Materialien, Tapeten, Schränken und Fensterbehandlungen ignoriert. *`angle`* Muss ein Vielfaches von 45 für wiederholbare Texturen sein, es sei denn, diese werden auf Fließlinien- oder Skizzenobjekte angewendet.

## Standard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, für keine Rotation.

## Verwandte Themen {#section-f73c00e9368b478dac1fd15bb4367a12}

[Anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
