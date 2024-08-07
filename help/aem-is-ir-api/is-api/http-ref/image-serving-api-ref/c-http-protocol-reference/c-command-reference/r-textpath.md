---
title: textPath
description: Textpfad. Gibt den Pfad an, der als Grundlinie für den Text verwendet werden soll, der mit textPs= bereitgestellt wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# textPath{#textpath}

Textpfad. Gibt den Pfad an, der als Grundlinie für den Text verwendet werden soll, der mit textPs= bereitgestellt wird.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Pfaddaten. </p></td> 
 </tr> 
</table>

Weitere Informationen, einschließlich einer Beschreibung von *`pathDefinition`*, finden Sie unter [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) .

>[!NOTE]
>
>Im Gegensatz zu `clipPath=` werden Textrfade nicht automatisch geschlossen, wenn am Ende eines Unterpfads &quot;z&quot;oder &quot;Z&quot;nicht angegeben ist.

*`pathDefinition`* kann mehrere Unterpfade enthalten. Text wird auf den Unterpfaden in der angegebenen Reihenfolge gerendert.

Die RTF-Befehle `\ql`, `\qc`, `\qr`, `\li` und `\ri` können verwendet werden, um den gerenderten Text entlang des Pfads zu positionieren.

## Eigenschaften {#section-068137df436c46b9b55d271eb60e7285}

Textebenenattribut ( nur `textPs=`). Wird von anderen Ebenen ignoriert. Gilt für `layer=comp` für `layer=0`. Wird ignoriert, wenn `textPs=` vorhanden ist.

Wenn eine Ebene sowohl `textPath=` als auch `textFlowPath=` enthält, wird ein Fehler zurückgegeben.

## Standard {#section-697b1f2cfc43498080a31327e6eb173d}

Keine, für Standardtextrendering.

## Verwandte Themen {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
