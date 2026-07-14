---
title: Glanz
description: Glanz der Materialoberfläche. Gibt den relativen Glanz der Materialoberfläche an. Wird verwendet, um die Beleuchtungskarte auszuwählen und das Rendering von Glanzeffekten und 3D-Reflexionen zu steuern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
TQID: 'https://experienceleague.adobe.com/-69G38JBpD4-X1wvkFtfvvZpdbHs7pcPiHnbNDgGRCA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# Glanz{#gloss}

Glanz der Materialoberfläche. Gibt den relativen Glanz der Materialoberfläche an. Wird verwendet, um die Beleuchtungskarte auszuwählen und das Rendering von Glanzeffekten und 3D-Reflexionen zu steuern.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Val</span> </span> </p></td> 
  <td class="stentry"> <p>Glanz (0…100 Prozent) oder -1 für den Standardwert (Referenz) Glanzwert. </p></td> 
 </tr> 
</table>

Höhere Glanzwerte verursachen in der Regel stärkere, schärfere Reflexionen und verstärken, wenn Glanzeffekte in der Vignette aktiviert sind, spiegelnde Highlights auf der Materialoberfläche, meist durch Erhöhung des Beleuchtungskontrasts. Jeder Materialtyp (`type=`) definiert einen minimalen und einen maximalen Render-Effekt. Bei einigen Materialtypen (z. B. Tapeten) hat `gloss=` nur minimale Auswirkungen auf das Erscheinungsbild des Render-Effekts, während bei anderen Materialtypen (z. B. Stein oder Keramik) der Effekt wesentlich ausgeprägter ist.

Wenn `illum=-1` und die Vignette mehrere Illumination Maps definiert, wählt `gloss=` die Illumination Map aus, die für den aktuellen Render-Vorgang verwendet wird. Der Renderer wählt die Beleuchtungskarte aus, deren Glanzwert am nächsten an dem angegebenen Glanz liegt.

`gloss=-1` Wählt den Referenzglanzwert der ausgewählten Beleuchtungskarte aus, wie er in den Ansichtseigenschaften der Vignette definiert ist. Dieser Wert stellt sicher, dass das Beleuchtungsdiagramm genau wie erstellt verwendet wird, ohne dass weitere Änderungen vorgenommen werden, auch wenn Glanzeffekte aktiviert sind. Falls `illum=-1`, wird der Referenzglanzwert der ersten Beleuchtungskarte in der Vignettenansicht verwendet.

## Eigenschaften {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Materialattribut. Ignoriert, wenn die Vignette nicht mehrere Beleuchtungszuordnungen definiert. Oder, falls `illum=` angegeben ist, wenn die Vignette keine 3D-Reflexionsdaten enthält. Oder wenn das aktuelle Objekt keine 3D-Reflexionen unterstützt oder wenn Glanzeffekte in der Vignette deaktiviert sind.

## Standard {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Wenn das Material auf einem Katalogeintrag basiert, andernfalls der Referenzglanzwert der Standardbeleuchtungskarte oder der durch `illum=` spezifizierten Beleuchtungskarte.

## Verwandte Themen {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [ough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)

