---
title: textPath
description: Textpfad. Gibt den Pfad an, der als Baseline für den mit textPs= bereitgestellten Text verwendet werden soll.
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

Textpfad. Gibt den Pfad an, der als Baseline für den mit textPs= bereitgestellten Text verwendet werden soll.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Pfaddaten. </p></td> 
 </tr> 
</table>

Siehe [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) für weitere Informationen, einschließlich einer Beschreibung der *`pathDefinition`*.

>[!NOTE]
>
>Im Gegensatz zu `clipPath=` werden Textpfade nicht automatisch geschlossen, wenn am Ende eines Unterpfads kein „z“ oder „Z“ angegeben ist.

*`pathDefinition`* können mehrere Unterpfade enthalten. Der Text wird in den Unterpfaden in der angegebenen Reihenfolge gerendert.

Die RTF-Befehle `\ql`, `\qc`, `\qr`, `\li` und `\ri` können verwendet werden, um den gerenderten Text entlang des Pfads zu positionieren.

## Eigenschaften {#section-068137df436c46b9b55d271eb60e7285}

Attribut der Textebene (nur `textPs=`). Von anderen Ebenen ignoriert. Gilt für `layer=0`, wenn für `layer=comp` angegeben. Ignoriert, wenn `textPs=` vorhanden sind.

Ein Fehler wird zurückgegeben, wenn eine Ebene sowohl `textPath=` als auch `textFlowPath=` enthält.

## Standard {#section-697b1f2cfc43498080a31327e6eb173d}

Keine, für die standardmäßige Textwiedergabe.

## Verwandte Themen {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
