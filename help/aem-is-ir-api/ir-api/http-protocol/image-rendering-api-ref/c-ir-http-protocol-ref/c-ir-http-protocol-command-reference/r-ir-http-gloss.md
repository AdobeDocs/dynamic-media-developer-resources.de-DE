---
description: Materialoberflächenglanz. Gibt die relative Glanz der Materialoberfläche an. Dient zur Auswahl der Beleuchtungskarte und zur Steuerung des Renderings von Glanzeffekten und 3D-Reflexionen.
seo-description: Materialoberflächenglanz. Gibt die relative Glanz der Materialoberfläche an. Dient zur Auswahl der Beleuchtungskarte und zur Steuerung des Renderings von Glanzeffekten und 3D-Reflexionen.
seo-title: gloss
solution: Experience Manager
title: gloss
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# gloss{#gloss}

Materialoberflächenglanz. Gibt die relative Glanz der Materialoberfläche an. Dient zur Auswahl der Beleuchtungskarte und zur Steuerung des Renderings von Glanzeffekten und 3D-Reflexionen.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Glanz (0...100 Prozent) oder -1 für den standardmäßigen (Referenz-) Glanz-Wert. </p></td> 
 </tr> 
</table>

Höhere Glanzwerte führen in der Regel zu stärkeren, schärferen Reflexionen und verstärken, wenn Glanzeffekte in der Vignette aktiviert sind, die Glanzlichter auf der Materialoberfläche, meist durch Erhöhung des Beleuchtungskontrasts. Jeder Materialtyp ( `type=`) definiert einen minimalen und einen maximalen Rendereffekt. Bei einigen Materialarten (z.B. Wandpapier) hat `gloss=` es kaum Auswirkungen auf das Aussehen des Rendereffekts, während bei anderen Materialtypen (z.B. Stein oder Keramik) der Effekt wesentlich ausgeprägter ist.

Wenn `illum=-1` und falls die Vignette mehrere Beleuchtungskarten definiert, `gloss=` wählt die für den aktuellen Rendervorgang verwendete Beleuchtungskarte aus. Der Renderer wählt die Beleuchtungszuordnung, deren Glanzwert dem angegebenen Glanz am nächsten kommt.

`gloss=-1` wählt den Referenzglanzwert der ausgewählten Lichtkarte aus, wie in den Eigenschaften für die Ansicht der Vignette definiert. Dadurch wird sichergestellt, dass die Beleuchtungskarte exakt wie verfasst verwendet wird, ohne dass weitere Änderungen vorgenommen werden, auch wenn Glanzeffekte aktiviert sind. Wenn `illum=-1` auch, wird der Referenzglanzwert der ersten Beleuchtungskarte in der Vignettenansicht verwendet.

## Eigenschaften {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Materialattribut. Wird ignoriert, wenn die Vignette keine mehrfachen Beleuchtungskarten definiert oder wenn angegeben `illum=` ist, wenn die Vignette keine 3D-Reflexionsdaten enthält oder wenn das aktuelle Objekt keine 3D-Reflexionen unterstützt oder wenn Glanzeffekte in der Vignette deaktiviert sind.

## Standard {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` wenn das Material auf einem Katalogeintrag basiert, andernfalls der Bezugsglanzwert der Standard-Beleuchtungskarte oder der Beleuchtungskarte, die durch `illum=`angegeben wird.

## Verwandte Themen {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
