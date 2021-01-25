---
description: Unschärfemaske. Bei "Unschärfe"wird die Ebene bzw. das letzte Bild der Ansicht nach der Skalierung maskiert, wenn layer=comp.
seo-description: Unschärfemaske. Bei "Unschärfe"wird die Ebene bzw. das letzte Bild der Ansicht nach der Skalierung maskiert, wenn layer=comp.
seo-title: op_usm
solution: Experience Manager
title: op_usm
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c647e063-2405-489b-b14d-a70638ac8af7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 7%

---


# op_usm{#op-usm}

Unschärfemaske. Bei &quot;Unschärfe&quot;wird die Ebene bzw. das letzte Bild der Ansicht nach der Skalierung maskiert, wenn layer=comp.

Es wird angenommen, dass die Parameter auf das Bild mit voller Auflösung angewendet werden und bei der Verarbeitung eines neu aufgenommenen Bildes verkleinert werden.

`op_usm= *``*[, *``*[, *``*[, *`amountTradiusthreoldmonochrom`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Betrag</span></span> </p></td> 
  <td class="stentry"> <p>Filterfestigkeitsfaktor (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Filterkernradius in Pixel (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Schwellenwert</span></span> </p></td> 
  <td class="stentry"> <p>Filterschwellenwert (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Monochrom</span></span> </p></td> 
  <td class="stentry"> <p>Auf 0 setzen, um jede Farbkomponente separat anzuwenden, oder auf 1, um nur die Bildhelligkeit (Intensität) anzuwenden. </p> <p> <span class="codeph"><span class="varname"> Bei Graustufenbildern werden </span></span> Monochrome ignoriert. </p></td> 
 </tr> 
</table>

Die Ebenenmaske oder die Composite-Maske wird ebenfalls scharfgezeichnet.

## Eigenschaften {#section-fb5311b34d164946b74dadb32359518a}

Ebenenattribut oder Ansicht-Attribut. Gilt für die aktuelle Ebene oder für die letzte Ansicht, wenn `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` für keine Unschärfemaske.

## Verwandte Themen {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
