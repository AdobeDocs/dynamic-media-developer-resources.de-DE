---
description: Unschärfemaske. Bei "Unschärfe"wird die Ebene bzw. das letzte Bild der Ansicht nach der Skalierung maskiert, wenn layer=comp.
seo-description: Unschärfemaske. Bei "Unschärfe"wird die Ebene bzw. das letzte Bild der Ansicht nach der Skalierung maskiert, wenn layer=comp.
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Scene7 Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---


# op_usmR{#op-usmr}

Unschärfemaske. Bei &quot;Unschärfe&quot;wird die Ebene bzw. das letzte Bild der Ansicht nach der Skalierung maskiert, wenn layer=comp.

Die Parameter werden wie bisher angewendet, unabhängig davon, ob ein Downsampling stattgefunden hat.

`op_usmR= *``*[, *``*[, *``*[, *`MentradiusRmomoldmonochrom`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Betrag</span></span> </p></td> 
  <td class="stentry"> <p>Filterfestigkeitsfaktor (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Filterkernradius in Pixel (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Schwellenwert</span></span> </p></td> 
  <td class="stentry"> <p>Filterschwellenwert (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Monochrom</span></span> </p></td> 
  <td class="stentry"> <p>Auf 0 setzen, um jede Farbkomponente separat anzuwenden, oder auf 1, um nur die Bildhelligkeit (Intensität) anzuwenden. </p> <p><span class="codeph"> <span class="varname"> Bei Graustufenbildern werden </span></span> Monochrome ignoriert. </p> </td> 
 </tr> 
</table>

Die Ebenenmaske oder die Composite-Maske wird ebenfalls scharfgezeichnet.

## Eigenschaften {#section-fb5311b34d164946b74dadb32359518a}

Ebenenattribut oder Ansicht-Attribut. Gilt für die aktuelle Ebene oder für die letzte Ansicht, wenn `layer=comp`. Effektebenen ignorieren dies.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` für keine Unschärfemaske.

## Verwandte Themen {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
