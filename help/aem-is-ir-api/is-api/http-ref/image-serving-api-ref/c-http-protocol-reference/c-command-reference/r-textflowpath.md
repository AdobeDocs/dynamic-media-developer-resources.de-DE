---
description: Textflussbereich. Gibt einen oder mehrere Regionen an, in die der mit textPs= angegebene Text fließen soll.
seo-description: Textflussbereich. Gibt einen oder mehrere Regionen an, in die der mit textPs= angegebene Text fließen soll.
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---


# textFlowPath{#textflowpath}

Textflussbereich. Gibt einen oder mehrere Regionen an, in die der mit textPs= angegebene Text fließen soll.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p> </td> 
 </tr> 
</table>

Weitere Informationen, einschließlich einer Beschreibung von *`pathDefinition`*, finden Sie unter [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d).

Die RTF-Randbefehle `\margl`, `\margr`, `\margt` und `\margb` werden ignoriert, wenn `textFlowPath=` vorhanden ist. Wenn keine Pfaddefinition angegeben ist, wird `textFlowPath=` ignoriert.

## Eigenschaften {#section-b68dc887c6534ce8982cad740b3aeaa4}

Textebenenattribut ( `textPs=` nur). Wird von anderen Ebenen ignoriert. Gilt für `layer=0`, wenn für `layer=comp` angegeben.

## Standard {#section-68c4559b9e8242059b82e5a39a455dfc}

Wie das Ebenenrechteck; Text füllt das gesamte Rechteck der Ebene.

## Verwandte Themen {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15),  [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
