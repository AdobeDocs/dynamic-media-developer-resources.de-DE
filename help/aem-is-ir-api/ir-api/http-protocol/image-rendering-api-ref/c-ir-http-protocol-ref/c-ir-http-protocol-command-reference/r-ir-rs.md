---
title: RS
description: Erweiterte Render-Einstellungen. Gibt beim Rendern der aktuellen Auswahl anzuwendende erweiterte Render-Einstellungen an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# RS{#rs}

Erweiterte Render-Einstellungen. Gibt beim Rendern der aktuellen Auswahl anzuwendende erweiterte Render-Einstellungen an.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Val</span> </p> </td> 
  <td class="stentry"> <p>Render settings string. </p></td> 
 </tr> 
</table>

Wird zur Feinabstimmung des Render-Erscheinungsbilds verwendet. Um Zeichenfolgen für Render-Einstellungen zu erstellen, verwenden Sie die Render-Funktion des Vignette Authoring-Tools (Teil des Dynamic Media Image Authoring-Pakets).

## Eigenschaften {#section-9a2b2228789046658cb80eddf343af75}

Materialattribut.

## Standard {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Beispiel {#section-47e4811882574441a4d517e42a35f352}

Nach einigen Experimenten in der Bildbearbeitung wird festgestellt, dass Unschärfemaske (USM) das richtige Maß an Scharfzeichnung für die jeweilige Anwendung und das jeweilige Material bietet. Die Zeichenfolge für die Render-Einstellungen, die USM konfiguriert, wird in den `rs=`-Befehl kopiert, der für dieses Material verwendet werden soll:

`…&rs=U2V20W50X2&…`

## Verwandte Themen {#section-930116e735024a008c994547ba36ee40}

[catalog:renderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
