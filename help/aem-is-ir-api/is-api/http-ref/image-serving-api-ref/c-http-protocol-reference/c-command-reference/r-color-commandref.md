---
description: Ebenenfarbe. Gibt die Vordergrundfarbe und Deckkraft von Volltonfarbe- und Effektebenen sowie die Feldfüllfarbe für Textebenen an.
seo-description: Ebenenfarbe. Gibt die Vordergrundfarbe und Deckkraft von Volltonfarbe- und Effektebenen sowie die Feldfüllfarbe für Textebenen an.
seo-title: Farbe
solution: Experience Manager
title: Farbe
topic: Scene7 Image Serving - Image Rendering API
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# color{#color}

Ebenenfarbe. Gibt die Vordergrundfarbe und Deckkraft von Volltonfarbe- und Effektebenen sowie die Feldfüllfarbe für Textebenen an.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Farbe </span></span> </p> </td> 
  <td class="stentry"> <p>Farbwert Grau, RGB oder CMYK, mit oder ohne Alpha. </p> </td> 
 </tr> 
</table>

Bei Bild- und Textebenen `color=` füllt transparente und halbtransparente Bereiche innerhalb des Begrenzungsrechtecks der Ebene mit der angegebenen Farbe* vor* `rotate=` und `extend=` werden angewendet.

## Eigenschaften {#section-d6e74c36a49547849212e4db8927e678}

Ebenenattribut. Gilt für die aktuelle Ebene oder für die Ebene 0, falls `layer=comp`dies der Fall ist.

*`color`* im Arbeitsfarbraum vorhanden ist, der dem Pixeltyp *`color`* entspricht. *`color`* wird genau konvertiert, wenn das Ebenenbild zum Zeitpunkt der Zusammenführung einen anderen Pixeltyp aufweist.

## Standard {#section-60611c72876b4c45b5c85ce35608e5ec}

Keine Standardeinstellung für Volltonfarben- und Effektebenen; muss eine Farbe angegeben werden. Die Standardeinstellung ist 0,0,0,0 (vollständig transparent) für Bild- und Textebenen.

## Beispiel {#section-2d090493f4ec4e188bbc5565aa151a05}

Im folgenden Vorlagenfragment setzen wir den Texthintergrund auf eine 50%ige undurchsichtige Farbe und verwenden dieselbe Farbe, um einen halbtransparenten 10-Pixel-Rand um das Bild der Ebene 2 hinzuzufügen:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Verwandte Themen {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Farbmanagement](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
