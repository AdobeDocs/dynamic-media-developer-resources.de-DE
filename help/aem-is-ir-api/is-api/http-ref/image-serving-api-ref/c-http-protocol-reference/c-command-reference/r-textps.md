---
title: textPs
description: Ebenentext (Adobe Photoshop-kompatibel). Gibt den Textkörper für eine Textebene an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
TQID: 'https://experienceleague.adobe.com/z5z7-6Pe4B-DUsxcspNcMxS-gXXo8Cv7stwBEMpxnNo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 3%

---

# textPs{#textps}

Ebenentext (Adobe Photoshop-kompatibel). Gibt den Textkörper für eine Textebene an.

`textPs= *`Zeichenfolge`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Zeichenfolge</span> </span> </p> </td> 
  <td class="stentry"> <p>Rich-Text-formatierte Zeichenfolge (RTF). </p></td> 
 </tr> 
</table>

Die gesamte Schriftart, Schriftfarbe und Absatzformatierung wird mithilfe von RTF-Befehlen gesteuert.

Siehe [Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` unterstützt erweiterte Funktionen wie Ausrichtung, Textfluss in nicht rechteckige Bereiche, die mit `textFlowPath=` und/oder `textFlowXPath=` definiert sind, und Rendering von Text entlang beliebiger, mit `textPath=` definierter Pfade.

## Eigenschaften {#section-a289dc26b6534b41998b1e241d5f2f92}

Ebenenattribut. Gilt für `layer=0`, falls `layer=comp`. Sich gegenseitig ausschließend mit `src=` und `text=` in derselben Ebene. Das letzte Vorkommen von `text=`, `textPs=` und `src=` hat Vorrang und bestimmt, ob es sich um ein Bild oder eine Textebene handelt. Von Effektebenen ignoriert.

## Standard {#section-11c2ae2c96d64a0a9c207252df663e4d}

Keine.

## Verwandte Themen {#section-5c2b25767d2b47b5be817271ab12e13c}

[Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
