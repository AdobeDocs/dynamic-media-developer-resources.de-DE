---
description: Hintergrundfarbe. Gibt die subtraktive Farbe für kolorierbare Texturen und Dekorationen an.
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---

# bgc{#bgc}

Hintergrundfarbe. Gibt die subtraktive Farbe für kolorierbare Texturen und Dekorationen an.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB- oder Graufarbwert. </p></td> 
 </tr> 
</table>

Der Texturkolorisierungsalgorithmus des Bild-Renderings ist ganz einfach - die Komponentenwerte von `bgc=` werden von denen der Texturpixel subtrahiert, `color=` wird hinzugefügt und schließlich wird das Ergebnis auf `0,0,0` und `255,255,255` gekürzt.

Für typische Verwendungen der Texturkolorisierung kann der Wert für `bgc=` die wichtigste oder dominierende Farbe im Texturbild sein. Dynamic Media Image Authoring bietet halbautomatische Tools, die vernünftige `bgc=` Farbwerte aus Texturbildern extrahieren.

Wenn ein Texturmaterial auf ein nicht texturierbares Vignettenobjekt angewendet wird, wird `bgc=` als Vordergrundfarbe angewendet, wenn `color=` nicht angegeben ist.

## Eigenschaften {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materialattribut. Ignoriert durch feste Farbe und Möbel.

## Standard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` wenn das Material auf einem Katalogeintrag basiert, andernfalls ( `bgc=808080` neutral gray).

## Beispiel {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Färben eines Bekleidungsgewebes, dessen Textur die dominierende RGB-Farbe hat 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Verwandte Themen {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
