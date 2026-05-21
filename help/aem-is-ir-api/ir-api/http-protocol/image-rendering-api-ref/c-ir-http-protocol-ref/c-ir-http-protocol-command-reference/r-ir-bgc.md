---
title: BGC
description: Hintergrundfarbe. Gibt die subtraktive Farbe für färbbare Texturen und Abziehbilder an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
TQID: 'https://experienceleague.adobe.com/0Er9kHrfQj1lt14SlNJHxqddJZOp8BaO-lLYSqc5ajU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 159
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

Für typische Anwendungen der Texturfärbung kann der Wert für `bgc=` die wichtigste oder dominanteste Farbe im Texturbild sein. Die Dynamic Media-Bildbearbeitung bietet halbautomatische Tools zum Extrahieren angemessener `bgc=`-Farbwerte aus Texturen und Bildern.

Wenn ein Texturmaterial auf ein nicht texturierbares Vignettenobjekt angewendet wird, wird `bgc=` als Vordergrundfarbe angewendet, wenn `color=` nicht angegeben ist.

## Eigenschaften {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materialattribut. Wird von einfarbigen und Schrankmaterialien ignoriert.

## Standard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Wenn das Material auf einem Katalogeintrag basiert, andernfalls `bgc=808080` (Neutralgrau).

## Beispiel {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Färben Sie ein Bekleidungsgewebe, dessen Textur die dominierende RGB-Farbe hat 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Verwandte Themen {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
