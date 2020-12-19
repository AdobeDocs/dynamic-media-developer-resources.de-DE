---
description: Hintergrundfarbe. Gibt die Subtraktionsfarbe für farbige Texturen und Dekore an.
seo-description: Hintergrundfarbe. Gibt die Subtraktionsfarbe für farbige Texturen und Dekore an.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 7%

---


# bgc{#bgc}

Hintergrundfarbe. Gibt die Subtraktionsfarbe für farbige Texturen und Dekore an.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB- oder Graufarbwert. </p></td> 
 </tr> 
</table>

Der Texturkolorisierungsalgorithmus des Image Rendering ist ganz einfach - die Komponentenwerte von `bgc=` werden von denen der Texturpixel abgezogen, `color=` hinzugefügt und schließlich wird das Ergebnis auf `0,0,0` und `255,255,255` geklickt.

Bei typischen Verwendungen der Texturfärbung ist der Wert für `bgc=` möglicherweise die wichtigste oder dominierende Farbe im Texturbild. Scene7 Image Authoring bietet halbautomatische Werkzeuge, mit denen Sie vernünftige `bgc=`-Farbwerte aus Texturbildern extrahieren können.

Wenn ein Texturmaterial auf ein nicht texturierbares Vignettenobjekt angewendet wird, wird `bgc=` als Vordergrundfarbe angewendet, wenn `color=` nicht angegeben ist.

## Eigenschaften {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materialattribut. Ingnotiert von festen Farben und Möbeln.

## Standard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` wenn das Material auf einem Katalogeintrag basiert, andernfalls  `bgc=808080` (neutral grau).

## Beispiel {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Färben eines Bekleidungsgewebes, dessen Textur die dominierende RGB-Farbe hat 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Verwandte Themen {#section-de9958dd63a742b4b5d780c59a57da33}

[Katalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
