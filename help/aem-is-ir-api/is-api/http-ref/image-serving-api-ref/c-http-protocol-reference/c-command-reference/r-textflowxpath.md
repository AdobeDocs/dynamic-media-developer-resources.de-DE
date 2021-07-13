---
description: Textflussausschlussbereich. Gibt einen oder mehrere Bereiche an, die vom Textfluss ausgeschlossen werden sollen.
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

---

# textFlowXPath{#textflowxpath}

Textflussausschlussbereich. Gibt einen oder mehrere Bereiche an, die vom Textfluss ausgeschlossen werden sollen.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Weitere Informationen, einschließlich einer Beschreibung von *`pathDefinition`*, finden Sie unter [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) . Wenn keine Pfaddefinition angegeben ist, wird `textFlowXPath=` ignoriert.

## Eigenschaften {#section-cd1ebb151d4a405fbfc508d46522d686}

Textebenenattribut ( nur `textPs=`). Wird von anderen Ebenen ignoriert oder wenn ohne `textFlowPath=` angegeben. Gilt für `layer=0`, falls für `layer=comp` angegeben.

## Standard {#section-9405cda904684d829ed12a9e40a4dc46}

Keine.

## Verwandte Themen {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
