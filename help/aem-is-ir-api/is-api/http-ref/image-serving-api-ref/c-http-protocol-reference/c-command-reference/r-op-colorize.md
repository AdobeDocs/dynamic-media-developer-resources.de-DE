---
title: op_colorize
description: Bild einfärben. Färbt die Bilddaten unter Beibehaltung von Schatten und Hervorhebungen ein.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

Bild einfärben. Färbt die Bilddaten unter Beibehaltung von Schatten und Hervorhebungen ein.

` op_colorize= *`Farbe`*[,off|norm[, *`Kontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Ersatz-RGB-Farbe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> von </span> </p> </td> 
  <td class="stentry"> <p>Automatische Helligkeitskompensation deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">-</span> </p> </td> 
  <td class="stentry"> <p>Automatische Helligkeitskompensation aktivieren (Standard). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Kontrast </span> </p> </td> 
  <td class="stentry"> <p>Kontrastbereich (real 0..100); auf 0 gesetzt, um den Eingangskontrast beizubehalten. </p> </td> 
 </tr> 
</table>

Das zweite Argument gibt an, ob die Helligkeit des Quellbilds vor der Einfärbung angepasst werden soll. Geben Sie `off` an, um die automatische Helligkeitskompensation zu deaktivieren, oder `norm`, um die Helligkeit automatisch so anzupassen, dass der Medianwert eine Intensität von 50 % hat.

Legen Sie den *`contrast`* auf 0 fest, um den Kontrastbereich des Eingabebilds beizubehalten, oder geben Sie einen gewünschten Kontrastbereich mit einem Wert größer als 0 an. Mit dem Wert 100 erzielen Sie den maximalen Kontrast. Typische Werte können zwischen 30 und 70 liegen.

Zusätzlich zu den integrierten Helligkeits- und Kontrasteinstellungen können `op_brightness=` und `op_contrast=` verwendet werden, um den Farbeffekt weiter zu optimieren.

>[!NOTE]
>
>Der Einfärbungsalgorithmus verwendet nur die Luminanzinformationen in den Bilddaten. Diese Konvertierung in Graustufen ist einfach und nicht farbgesteuert. `op_colorize` gibt immer RGB-Daten aus, auch wenn die Eingabe Graustufen oder CMYK ist.

## Eigenschaften {#section-c0f8bd424b864153a1108f384939f55b}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert.

*`color`* muss ein RGB-Wert sein. Graue oder CMYK-*`color`* werden nicht unterstützt.

Der *`contrast`* wird ignoriert, wenn die Helligkeitskompensation deaktiviert ist.

Es wird davon ausgegangen, dass *`color`* im Arbeitsfarbraum vorhanden ist, der dem Pixeltyp des *`color`* entspricht. *`color`* wird genau konvertiert, wenn das Ebenenbild zum Zeitpunkt der Zusammenführung einen anderen Pixeltyp aufweist.

CMYK-Bilder werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Standard {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, für keine Einfärbung. Das zweite und dritte Argument setzen für eine automatische Helligkeitskompensation und keine Kontraständerung auf `norm,0`.

## Beispiel {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Passen Sie Helligkeit und Kontrast dynamisch an, bevor Sie eine Bildebene einfärben:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Verwenden Sie stattdessen die automatische Helligkeits- und Kontrasteinstellung:

… `&op_colorize=a0b0c0,norm,50&`…

## Verwandte Themen {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_bright=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
