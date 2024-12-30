---
title: BGC
description: Hintergrundfarbe. Gibt die subtraktive Farbe für färbbare Texturen und Abziehbilder an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# BGC {#bgc}

Hintergrundfarbe. Gibt die subtraktive Farbe für färbbare Texturen und Abziehbilder an.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> Farbe</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB- oder Grauwert. </p></td> 
 </tr> 
</table>

Der Textur-Farbalgorithmus des Bild-Renderings ist einfach. Die Komponentenwerte von `bgc=` werden von den Werten der Textur-Pixel subtrahiert. `color=` wird hinzugefügt und das Ergebnis wird schließlich auf `0,0,0` und `255,255,255` abgeschnitten.

Für typische Anwendungen der Texturfärbung kann der Wert für `bgc=` die wichtigste oder dominanteste Farbe im Texturbild sein. Die Dynamic Media-Bildbearbeitung bietet halbautomatische Tools, die angemessene `bgc=` aus Bildtexturen extrahieren.

Wenn ein Texturmaterial auf ein nicht texturierbares Vignettenobjekt angewendet wird, wird `bgc=` als Vordergrundfarbe angewendet, wenn `color=` nicht angegeben ist.

## Eigenschaften {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materialattribut. Wird von einfarbigen und Schrankmaterialien ignoriert.

## Standard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Wenn das Material auf einem Katalogeintrag basiert, andernfalls `bgc=808080` (Neutralgrau).

## Beispiel {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Färben Sie ein Bekleidungsgewebe, dessen Textur die dominante RGB-Farbe hat 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Verwandte Themen {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
