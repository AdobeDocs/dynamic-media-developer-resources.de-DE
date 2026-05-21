---
title: Farbe
description: Ebenenfarbe. Gibt die Vordergrundfarbe und Deckkraft von Volltonfarbe- und Effektebenen sowie die Textfeldfüllfarbe für Textebenen an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
TQID: 'https://experienceleague.adobe.com/tjiZfVTztBPgsIYS1SGtVeBxo0Wq1q8Ur-kq3Xtm6og'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 3%

---

# Farbe{#color}

Ebenenfarbe. Gibt die Vordergrundfarbe und Deckkraft von Volltonfarbe- und Effektebenen sowie die Textfeldfüllfarbe für Textebenen an.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Farbe </span> </span> </p> </td> 
  <td class="stentry"> <p>Grau, RGB oder CMYK-Farbwert, mit oder ohne Alpha. </p> </td> 
 </tr> 
</table>

Wenn Bild- und Textebenen vorhanden sind, füllt `color=` transparente und halb-deckende Bereiche innerhalb des umgebenden Rechtecks der Ebene mit der angegebenen Farbe*, bevor* `rotate=` und `extend=` angewendet werden.

## Eigenschaften {#section-d6e74c36a49547849212e4db8927e678}

Ebenenattribut. Gilt für die aktuelle Ebene oder für Ebene 0, falls `layer=comp`.

Es wird davon ausgegangen, dass der Modifikator *`color`* in dem dem Pixeltyp des *`color`* entsprechenden Arbeitsfarbraum vorhanden ist. Und *`color`* wird genau konvertiert, wenn das Ebenenbild zum Zeitpunkt der Zusammenführung einen anderen Pixeltyp aufweist.

## Standard {#section-60611c72876b4c45b5c85ce35608e5ec}

Kein Standard für Volltonfarbe- und Effektebenen. Es muss eine Farbe angegeben werden. Die Standardeinstellung ist 0,0,0,0 (vollständig transparent) für Bild- und Textebenen.

## Beispiel {#section-2d090493f4ec4e188bbc5565aa151a05}

Im folgenden Vorlagenfragment ist der Texthintergrund auf eine 50 % opake Farbe festgelegt und verwendet dieselbe Farbe, um einen halbtransparenten 10-Pixel-Rahmen um das Bild der Ebene 2 hinzuzufügen:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Verwandte Themen {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [Extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
