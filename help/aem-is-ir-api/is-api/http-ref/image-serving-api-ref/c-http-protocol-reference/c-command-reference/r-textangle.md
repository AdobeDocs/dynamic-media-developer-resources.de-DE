---
description: Text-Rendering-Richtung. Gibt den Winkel an, bei dem mit textPs= angegebener Text im Textfeld angeordnet und gerendert wird (definiert mit size= oder textFlowPath=).
solution: Experience Manager
title: textAngle
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 5%

---

# textAngle{#textangle}

Text-Rendering-Richtung. Gibt den Winkel an, bei dem mit textPs= angegebener Text im Textfeld angeordnet und gerendert wird (definiert mit size= oder textFlowPath=).

` textAngle= *`Winkel`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Winkel </span> </p> </td> 
  <td class="stentry"> <p>Richtungswinkel (Grad). </p> </td> 
 </tr> 
</table>

Bei positiven Werten wird der Text im Uhrzeigersinn gedreht. `textAngle=90` zeichnet Text von oben nach unten.

## Eigenschaften {#section-6d586a632daa4261a8ce62db56140b36}

Ebenenattribut. Gilt für `layer=0`, wenn `layer=comp`. Wird ignoriert, wenn `textPs=` nicht für diese Ebene angegeben ist oder `textPath=` angegeben ist.

## Standard {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` für keine Rotation.

## Verwandte Themen {#section-dccc29ff33704061b2519b56b7be45fd}

[Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [Textpositionierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
