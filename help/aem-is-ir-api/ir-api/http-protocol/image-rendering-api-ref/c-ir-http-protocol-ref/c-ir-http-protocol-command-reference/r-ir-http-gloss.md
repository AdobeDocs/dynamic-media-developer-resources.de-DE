---
title: Glanz
description: Materialoberflächenglanz. Gibt das relative Glanz der Materialoberfläche an. Wird verwendet, um die Beleuchtungskarte auszuwählen und das Rendering von Glanzeffekten und 3D-Reflexionen zu steuern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---

# Glanz{#gloss}

Materialoberflächenglanz. Gibt das relative Glanz der Materialoberfläche an. Wird verwendet, um die Beleuchtungskarte auszuwählen und das Rendering von Glanzeffekten und 3D-Reflexionen zu steuern.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Glanz (0...100 Prozent) oder -1 für den standardmäßigen Glanzwert (Referenz). </p></td> 
 </tr> 
</table>

Höhere Glanzwerte verursachen in der Regel stärkere, schärfere Reflexionen und verstärken, wenn Glanzeffekte in der Vignette aktiviert sind, die spekulären Highlights auf der Materialoberfläche, meist durch Erhöhung des Beleuchtungskontrasts. Jeder Werkstofftyp ( `type=`) definiert einen minimalen und einen maximalen Rendereffekt. Für einige Materialtypen (z. B. Wandpapier): `gloss=` hat kaum Auswirkungen auf das Erscheinungsbild des Rendereffekts, während bei anderen Materialtypen (z. B. Stein oder Keramik) der Effekt wesentlich ausgeprägter ist.

Wenn `illum=-1` und wenn die Vignette mehrere Beleuchtungskarten definiert, `gloss=` wählt die für den aktuellen Rendervorgang verwendete Beleuchtungskarte aus. Der Renderer wählt die Beleuchtungskarte aus, deren Glanzwert dem angegebenen Glanz am nächsten kommt.

`gloss=-1` Wählt den Referenzglanzwert der ausgewählten Beleuchtungskarte aus, wie in den Ansichtseigenschaften der Vignette definiert. Dieser Wert stellt sicher, dass die Beleuchtungskarte exakt wie verfasst verwendet wird, ohne weitere Änderungen vorzunehmen, auch wenn Glanzeffekte aktiviert sind. Wenn `illum=-1` dann wird der Referenzglanzwert der ersten Beleuchtungskarte in der Vignettenansicht verwendet.

## Eigenschaften {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Materialattribut. Wird ignoriert, wenn die Vignette nicht mehrere Beleuchtungskarten definiert. Oder wenn `illum=` angegeben ist, wenn die Vignette keine 3D-Reflektionsdaten enthält. Oder wenn das aktuelle Objekt keine 3D-Reflexionen unterstützt oder wenn Glanzeffekte in der Vignette deaktiviert sind.

## Standard {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Wenn das Material auf einem Katalogeintrag basiert, andernfalls der Referenzwert des Glanzwerts der Standardbeleuchtung oder der Beleuchtungskarte, die durch `illum=`.

## Verwandte Themen {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
