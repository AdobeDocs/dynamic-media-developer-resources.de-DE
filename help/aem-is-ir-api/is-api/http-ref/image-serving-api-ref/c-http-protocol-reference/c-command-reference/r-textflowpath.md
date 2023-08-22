---
title: textFlowPath
description: Textflussbereich. Gibt einen oder mehrere Bereiche an, in die der mit textPs= angegebene Text fließen soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---

# textFlowPath{#textflowpath}

Textflussbereich. Gibt einen oder mehrere Bereiche an, in die der mit textPs= angegebene Text fließen soll.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p> </td> 
 </tr> 
</table>

Siehe [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) für zusätzliche Informationen, einschließlich einer Beschreibung von *`pathDefinition`*.

Die RTF-Margenbefehle `\margl`, `\margr`, `\margt`, und `\margb` werden ignoriert, wenn `textFlowPath=` vorhanden ist. Wenn keine Pfaddefinition angegeben ist, `textFlowPath=` wird ignoriert.

## Eigenschaften {#section-b68dc887c6534ce8982cad740b3aeaa4}

Textebenen-Attribut ( `textPs=` nur). Wird von anderen Ebenen ignoriert. Gilt für `layer=0` sofern für `layer=comp`.

## Standard {#section-68c4559b9e8242059b82e5a39a455dfc}

Entspricht dem Ebenenrechteck; Text füllt das gesamte Ebenenrechteck.

## Verwandte Themen {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
