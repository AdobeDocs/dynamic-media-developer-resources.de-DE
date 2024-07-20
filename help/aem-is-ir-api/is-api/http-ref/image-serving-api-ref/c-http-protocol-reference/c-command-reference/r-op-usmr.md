---
title: op_usmR
description: Unschärfemaske. Unschärfe maskiert die Ebene oder das endgültige Ansichtsbild nach der Skalierung, wenn layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# op_usmR{#op-usmr}

Unschärfemaske. Unschärfe maskiert die Ebene oder das endgültige Ansichtsbild nach der Skalierung, wenn layer=comp.

Die Parameter werden unverändert angewendet, unabhängig davon, ob eine Downsampling-Analyse stattgefunden hat.

`op_usmR= *`amount`*[, *`radiusR`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> amount</span></span> </p></td> 
  <td class="stentry"> <p>Filterstärke (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Filtern Sie den Kernel-Radius in Pixel (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> threshold</span></span> </p></td> 
  <td class="stentry"> <p>Filterschwellenwert (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Legen Sie den Wert auf 0 fest, um auf jede Farbkomponente separat anzuwenden, oder auf 1, um nur auf die Bildhelligkeit (Intensität) anzuwenden. </p> <p><span class="codeph"> <span class="varname"> monochrome </span></span> wird bei Graustufenbildern ignoriert. </p> </td> 
 </tr> 
</table>

Die Ebenenmaske oder die zusammengesetzte Maske wird ebenfalls scharfgezeichnet.

## Eigenschaften {#section-fb5311b34d164946b74dadb32359518a}

Ebenenattribut oder Ansichtsattribut. Gilt für die aktuelle Ebene oder für das endgültige Ansichtsbild, wenn `layer=comp`. Effektebenen ignorieren dies.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` für keinen unscharfen Maskierungseffekt.

## Verwandte Themen {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
