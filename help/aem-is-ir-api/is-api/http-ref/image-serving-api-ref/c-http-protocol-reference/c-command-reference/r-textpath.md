---
description: Textpfad. Gibt den Pfad an, der als Grundlage für den mit textPs= bereitgestellten Text verwendet werden soll.
seo-description: Textpfad. Gibt den Pfad an, der als Grundlage für den mit textPs= bereitgestellten Text verwendet werden soll.
seo-title: textPath
solution: Experience Manager
title: textPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a2f0047b-ad62-4605-a723-b43d53fbea56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---


# textPath{#textpath}

Textpfad. Gibt den Pfad an, der als Grundlage für den mit textPs= bereitgestellten Text verwendet werden soll.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Weitere Informationen, einschließlich einer Beschreibung von *`pathDefinition`*, finden Sie unter [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d).

>[!NOTE]
>
>Im Gegensatz zu `clipPath=` werden Textpfade nicht automatisch geschlossen, wenn &#39;z&#39; oder &#39;Z&#39; am Ende eines Unterpfads nicht angegeben ist.

*`pathDefinition`* kann mehrere Unterpfade enthalten. Der Text wird auf den Unterpfaden in der angegebenen Reihenfolge gerendert.

Die RTF-Befehle `\ql`, `\qc`, `\qr`, `\li` und `\ri` können verwendet werden, um den gerenderten Text entlang dem Pfad zu positionieren.

## Eigenschaften {#section-068137df436c46b9b55d271eb60e7285}

Textebenenattribut ( `textPs=` nur). Wird von anderen Ebenen ignoriert. Gilt für `layer=0`, wenn für `layer=comp` angegeben. Wird ignoriert, wenn `textPs=` vorhanden ist.

Wenn eine Ebene sowohl `textPath=` als auch `textFlowPath=` enthält, wird ein Fehler zurückgegeben.

## Standard {#section-697b1f2cfc43498080a31327e6eb173d}

Keine, für Standard-Textwiedergabe.

## Verwandte Themen {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
