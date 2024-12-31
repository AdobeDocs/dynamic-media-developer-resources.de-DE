---
title: op_usmR
description: Unschärfemaske. Unschärfemasken maskieren die Ebene oder das endgültige Ansichtsbild, nach allen Skalierungen, wenn Layer=Comp.
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

Unschärfemaske. Unschärfemasken maskieren die Ebene oder das endgültige Ansichtsbild, nach allen Skalierungen, wenn Layer=Comp.

Die Parameter werden unverändert angewendet, unabhängig davon, ob ein Downsampling stattgefunden hat.

`op_usmR= *`amount`*[, *`radiusR`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Betrag</span></span> </p></td> 
  <td class="stentry"> <p>Filterstärkefaktor (real 0…5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>Filterkernradius in Pixeln (real 0…250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Schwellenwert</span></span> </p></td> 
  <td class="stentry"> <p>Filterschwellenwert (int 0…255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrom</span></span> </p></td> 
  <td class="stentry"> <p>Legen Sie hierfür 0 fest, um sie auf jede Farbkomponente separat anzuwenden, oder 1, um sie nur auf die Bildhelligkeit (Intensität) anzuwenden. </p> <p><span class="codeph"> <span class="varname"> Schwarzweiß</span></span> wird bei Graustufenbildern ignoriert. </p> </td> 
 </tr> 
</table>

Die Ebenenmaske bzw. Verbundmaske wird ebenfalls geschärft.

## Eigenschaften {#section-fb5311b34d164946b74dadb32359518a}

Ebenenattribut oder Ansichtsattribut. Gilt für die aktuelle Ebene oder, falls `layer=comp`, für das endgültige Ansichtsbild. Effektebenen ignorieren sie.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` für keinen Unschärfemaskeffekt.

## Verwandte Themen {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
