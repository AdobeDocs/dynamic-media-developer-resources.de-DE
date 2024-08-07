---
title: bgc
description: Hintergrundfarbe. Gibt die subtraktive Farbe für kolorierbare Texturen und Dekorationen an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# bgc {#bgc}

Hintergrundfarbe. Gibt die subtraktive Farbe für kolorierbare Texturen und Dekorationen an.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB oder grau. </p></td> 
 </tr> 
</table>

Der Texturkolorisierungsalgorithmus des Bild-Renderings ist unkompliziert - die Komponentenwerte von `bgc=` werden von den Werten der Texturpixel subtrahiert; `color=` wird hinzugefügt und schließlich wird das Ergebnis auf `0,0,0` und `255,255,255` abgeschnitten.

Für typische Verwendungen der Texturkolorisierung kann der Wert für `bgc=` die wichtigste oder dominante Farbe im Texturbild sein. Dynamic Media Image Authoring bietet halbautomatische Tools, die angemessene `bgc=` Farbwerte aus Texturbildern extrahieren.

Wenn ein Texturmaterial auf ein nicht texturierbares Vignettenobjekt angewendet wird, wird `bgc=` als Vordergrundfarbe angewendet, wenn `color=` nicht angegeben ist.

## Eigenschaften {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materialattribut. Ignoriert durch feste Farbe und Möbel.

## Standard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Wenn das Material auf einem Katalogeintrag basiert, andernfalls `bgc=808080` (neutral grau).

## Beispiel {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Färben eines Bekleidungsgewebes, dessen Textur die dominierende RGB-Farbe 120,34,193 aufweist:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Verwandte Themen {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
