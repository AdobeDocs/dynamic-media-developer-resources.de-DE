---
description: Unschärfemaske. Unschärfe maskiert die Ebene oder das endgültige Ansichtsbild nach der Skalierung, wenn layer=comp.
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 6%

---

# op_usm{#op-usm}

Unschärfemaske. Unschärfe maskiert die Ebene oder das endgültige Ansichtsbild nach der Skalierung, wenn layer=comp.

Es wird angenommen, dass die Parameter auf das Bild mit voller Auflösung angewendet und bei der Verarbeitung eines heruntergesampelten Bildes herabskaliert werden.

`op_usm= *``*[, *``*[, *``*[, *`amount tradiusdreoldmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Betrag</span></span> </p></td> 
  <td class="stentry"> <p>Filterfestigkeitsfaktor (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Filtern Sie den Kernel-Radius in Pixel (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Schwellenwert</span></span> </p></td> 
  <td class="stentry"> <p>Filterschwellenwert (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Legen Sie den Wert auf 0 fest, um auf jede Farbkomponente separat anzuwenden, oder auf 1, um nur auf die Bildhelligkeit (Intensität) anzuwenden. </p> <p> <span class="codeph"><span class="varname"> </span></span> Monochromeien werden bei Graustufenbildern ignoriert. </p></td> 
 </tr> 
</table>

Die Ebenenmaske oder die zusammengesetzte Maske wird ebenfalls scharfgezeichnet.

## Eigenschaften {#section-fb5311b34d164946b74dadb32359518a}

Ebenenattribut oder Ansichtsattribut. Gilt für die aktuelle Ebene oder für das endgültige Ansichtsbild, wenn `layer=comp` Wird von Effektebenen ignoriert.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` keine Unschärfemaske.

## Verwandte Themen {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
