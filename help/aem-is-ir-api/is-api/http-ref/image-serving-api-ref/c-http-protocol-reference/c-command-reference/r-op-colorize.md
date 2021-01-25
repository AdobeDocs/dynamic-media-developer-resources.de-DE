---
description: Bild färben. Färbt die Bilddaten und behält gleichzeitig die Schatten und Lichter bei.
seo-description: Bild färben. Färbt die Bilddaten und behält gleichzeitig die Schatten und Lichter bei.
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 4%

---


# op_colorize{#op-colorize}

Bild färben. Färbt die Bilddaten und behält gleichzeitig die Schatten und Lichter bei.

` op_colorize= *``*[,off|norm[, *`Farbkontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Ersatzfarbe RGB </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> aus </span> </p> </td> 
  <td class="stentry"> <p>Deaktivieren Sie die automatische Helligkeitskompensation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
  <td class="stentry"> <p>Automatischer Helligkeitsausgleich aktivieren (Standard). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Kontrast </span> </p> </td> 
  <td class="stentry"> <p>Kontrastbereich (real 0.100); auf 0 gesetzt, um den Kontrast der Eingabe beizubehalten. </p> </td> 
 </tr> 
</table>

Das zweite Argument gibt an, ob die Helligkeit des Quellbilds vor dem Färben angepasst werden soll. Geben Sie `off` an, um die automatische Helligkeitskompensation zu deaktivieren, oder `norm`, um die Helligkeit automatisch so anzupassen, dass der Medianwert bei 50 % liegt.

Setzen Sie den Wert *`contrast`* auf 0, um den Kontrastbereich des Eingabebilds beizubehalten, oder geben Sie einen gewünschten Kontrastbereich mit einem Wert größer als 0 an. Mit dem Wert 100 erzielen Sie den maximalen Kontrast. Typische Werte können zwischen 30 und 70 liegen.

Zusätzlich zu den integrierten Helligkeits- und Kontrastanpassungen können `op_brightness=` und `op_contrast=` verwendet werden, um den Färbeeffekt weiter anzupassen.

>[!NOTE]
>
>Der Farbalgorithmus verwendet nur die Luminanzinformationen in den Bilddaten. Diese Konvertierung in Graustufen ist einfach und nicht farbgesteuert. `op_colorize` gibt immer RGB-Daten aus, auch wenn die Eingabe Graustufen oder CMYK ist.

## Eigenschaften {#section-c0f8bd424b864153a1108f384939f55b}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`. Von Effektebenen ignoriert.

*`color`* muss ein RGB-Wert sein; Grau- oder CMYK- *`color`* Werte werden nicht unterstützt.

Der Wert *`contrast`* wird ignoriert, wenn die Helligkeitskompensation deaktiviert ist.

*`color`* im Arbeitsfarbraum vorhanden ist, der dem Pixeltyp  *`color`* entspricht. *`color`* wird genau konvertiert, wenn das Ebenenbild zum Zeitpunkt der Zusammenführung einen anderen Pixeltyp aufweist.

CMYK-Bilder werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Standard {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, für keine Färbung. Das zweite und dritte Argument sind standardmäßig auf `norm,0` eingestellt, um eine automatische Helligkeitskompensation zu erhalten und keinen Kontrast zu ändern.

## Beispiel {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Passen Sie die Helligkeit und den Kontrast dynamisch an, bevor Sie eine Bildebene färben:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Verwenden Sie stattdessen die automatische Helligkeits- und Kontrasteinstellung:

... `&op_colorize=a0b0c0,norm,50&`...

## Verwandte Themen {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contents=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d),  [Farbmanagement](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
