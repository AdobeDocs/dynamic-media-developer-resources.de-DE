---
title: op_colorize
description: Bild färben. Colorisiert die Bilddaten und behält gleichzeitig Schatten und Highlights bei.
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

Bild färben. Colorisiert die Bilddaten und behält gleichzeitig Schatten und Highlights bei.

` op_colorize= *`Farbe`*[,off|norm[, *`Kontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Ersatzfarbe RGB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
  <td class="stentry"> <p>Deaktivieren Sie die automatische Helligkeitskompensation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
  <td class="stentry"> <p>Automatische Helligkeitskompensation aktivieren (Standard). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Kontrast </span> </p> </td> 
  <td class="stentry"> <p>Kontrastbereich (real 0.100); auf 0 setzen, um den eingegebenen Kontrast beizubehalten. </p> </td> 
 </tr> 
</table>

Das zweite Argument gibt an, ob die Helligkeit des Quellbilds vor dem Einfärben angepasst werden soll. Geben Sie `off` an, um die automatische Helligkeitskompensation zu deaktivieren, oder `norm`, um die Helligkeit automatisch so anzupassen, dass der Medianwert 50 % beträgt.

Setzen Sie den Wert *`contrast`* auf 0, um den Kontrastbereich des Eingabebilds beizubehalten, oder legen Sie einen gewünschten Kontrastbereich mit einem Wert größer als 0 fest. Mit dem Wert 100 erzielen Sie den maximalen Kontrast. Typische Werte können zwischen 30 und 70 liegen.

Zusätzlich zu den integrierten Helligkeits- und Kontrastanpassungen können `op_brightness=` und `op_contrast=` verwendet werden, um den Farbeffekt weiter anzupassen.

>[!NOTE]
>
>Der Farbalgorithmus verwendet nur die Luminanzinformationen in den Bilddaten. Diese Konvertierung in Graustufen ist einfach und nicht farbgesteuert. `op_colorize` gibt immer RGB-Daten aus, auch wenn die Eingabe Graustufen- oder CMYK-Dateien enthält.

## Eigenschaften {#section-c0f8bd424b864153a1108f384939f55b}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp` Wird von Effektebenen ignoriert.

*`color`* muss ein RGB-Wert sein; grau oder CMYK *`color`* -Werte werden nicht unterstützt.

Der Wert *`contrast`* wird ignoriert, wenn die Helligkeitskompensation deaktiviert ist.

Es wird angenommen, dass *`color`* im Arbeitsfarbraum vorhanden ist, der dem Pixeltyp von *`color`* entspricht. *`color`* wird genau konvertiert, wenn das Ebenenbild zum Zeitpunkt der Zusammenführung einen anderen Pixeltyp aufweist.

CMYK-Bilder werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Standard {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, für keine Verfärbung. Das zweite und dritte Argument sind standardmäßig `norm,0`, da die Helligkeit automatisch ausgeglichen und der Kontrast nicht verändert wird.

## Beispiel {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Passen Sie die Helligkeit und den Kontrast dynamisch an, bevor Sie eine Bildebene färben:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&` ...

Verwenden Sie stattdessen die automatische Helligkeits- und Kontrasteinstellung:

... `&op_colorize=a0b0c0,norm,50&` ...

## Verwandte Themen {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Farbmanagement](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
