---
description: Erweiterte Rendereinstellungen. Gibt erweiterte Rendereinstellungen an, die beim Rendern der aktuellen Auswahl angewendet werden.
seo-description: Erweiterte Rendereinstellungen. Gibt erweiterte Rendereinstellungen an, die beim Rendern der aktuellen Auswahl angewendet werden.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# rs{#rs}

Erweiterte Rendereinstellungen. Gibt erweiterte Rendereinstellungen an, die beim Rendern der aktuellen Auswahl angewendet werden.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Zeichenfolge für Rendereinstellungen. </p></td> 
 </tr> 
</table>

Dient zum Optimieren des Renderscheins. Verwenden Sie die Renderfunktion des Vignette Authoring-Tools (Teil des Scene7 Image Authoring-Pakets), um Zeichenfolgen für Rendereinstellungen zu erstellen.

## Eigenschaften {#section-9a2b2228789046658cb80eddf343af75}

Materialattribut.

## Standard {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Beispiel {#section-47e4811882574441a4d517e42a35f352}

Nach einigen Experimenten im Image Authoring wird festgestellt, dass die Unschärfemaske (USM) die richtige Scharfzeichnung für die jeweilige Anwendung und das Material bereitstellt. Die Zeichenfolge für die Rendereinstellungen, die USM konfiguriert, wird zur Verwendung mit diesem Material in den Befehl `rs=` kopiert:

`…&rs=U2V20W50X2&…`

## Verwandte Themen {#section-930116e735024a008c994547ba36ee40}

[Katalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
