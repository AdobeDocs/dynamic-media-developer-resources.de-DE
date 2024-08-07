---
title: Text
description: Ebenentext. Gibt Text und Formatierungsinhalt für eine Textebene an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---

# Text{#text}

Ebenentext. Gibt Text und Formatierungsinhalt für eine Textebene an.

` text= *`string`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> string </span> </p> </td> 
  <td class="stentry"> <p>RTF-Zeichenfolge (Rich-Text-Format) oder Text-Zeichenfolge. </p> </td> 
 </tr> 
</table>

Die gesamte Steuerung der Schriftart-, Schriftfarbe- und Absatzformatierung erfolgt mithilfe von RTF-Befehlen. Weitere Informationen finden Sie unter [Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) .

`text=` unterstützt die automatische Skalierung des Textes, um das mit `size=` angegebene Ebenenrechteck auszufüllen.

Siehe [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` unterstützt die automatische Skalierung der Textebene, um den gerenderten Text anzupassen (wenn `size=` nicht angegeben ist oder nur die Breite angegeben ist). Beachten Sie, dass in diesem Fall nur einer der RTF-Ausrichtungsbefehle `\ql`, `\qr` und `\qc` angewendet werden kann. Andernfalls wird ein Fehler zurückgegeben.

## Eigenschaften {#section-8c0f020094a44c6b858454ef91ab4edf}

Ebenenattribut. Gilt für `layer=0` , wenn `layer=comp`. Gegenseitig mit `src=` und `textPs=` in derselben Ebene ausschließen; das letzte Vorkommen von `text=`, `textPs=` und `src=` hat Vorrang und bestimmt, ob es sich um ein Bild oder eine Textebene handelt. Wird von Effektebenen ignoriert.

## Standard {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Keine.

## Beispiel {#section-d011f765ec5c418d814a821019b0eef0}

Siehe Beispiele in [Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) und [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-207b779ab67342a5acd343e6bcc749c4}

[Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Textpositionierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
