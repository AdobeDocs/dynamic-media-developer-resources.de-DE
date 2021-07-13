---
description: Erweiterte Rendereinstellungen. Gibt erweiterte Rendereinstellungen an, die beim Rendern der aktuellen Auswahl angewendet werden sollen.
solution: Experience Manager
title: rs
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# rs{#rs}

Erweiterte Rendereinstellungen. Gibt erweiterte Rendereinstellungen an, die beim Rendern der aktuellen Auswahl angewendet werden sollen.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Zeichenfolge für Rendereinstellungen. </p></td> 
 </tr> 
</table>

Wird zur Feinabstimmung des Renderscheins verwendet. Verwenden Sie die Renderfunktion des Vignette Authoring-Tools (Teil des Dynamic Media Image Authoring-Pakets), um Rendereinstellungszeichenfolgen zu erstellen.

## Eigenschaften {#section-9a2b2228789046658cb80eddf343af75}

Materialattribut.

## Standard {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Beispiel {#section-47e4811882574441a4d517e42a35f352}

Nach einigen Experimenten mit der Bildbearbeitung wird festgestellt, dass die Unschärfemaske (USM) die korrekte Scharfzeichnung für die jeweilige Anwendung und das Material bereitstellt. Die Zeichenfolge der Render-Einstellungen, die USM konfiguriert, wird in den Befehl `rs=` kopiert, um sie mit diesem Material zu verwenden:

`…&rs=U2V20W50X2&…`

## Verwandte Themen {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
