---
description: Ebenentext. Gibt Text und Formatierungsinhalte für eine Textebene an.
seo-description: Ebenentext. Gibt Text und Formatierungsinhalte für eine Textebene an.
seo-title: Text
solution: Experience Manager
title: Text
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 6%

---


# Text{#text}

Ebenentext. Gibt Text und Formatierungsinhalte für eine Textebene an.

` text= *`Zeichenfolge`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Zeichenfolge </span> </p> </td> 
  <td class="stentry"> <p>RTF-Zeichenfolge oder Klartext-Zeichenfolge. </p> </td> 
 </tr> 
</table>

Alle Steuerelemente für Schriftart, Schriftfarbe und Absatzformatierung werden mithilfe von RTF-Befehlen erreicht. Weitere Informationen finden Sie unter [Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`text=` unterstützt die automatische Skalierung des Textes, um das angegebene Ebenenrechteck auszufüllen  `size=`.

Siehe [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` unterstützt die automatische Größenanpassung der Textebene, um den gerenderten Text einzupassen (wenn  `size=` keine Angabe erfolgt oder nur die Breite angegeben ist). Beachten Sie, dass in diesem Fall nur die RTF-Ausrichtungsbefehle `\ql`, `\qr` und `\qc` angewendet werden können. Andernfalls wird ein Fehler zurückgegeben.

## Eigenschaften {#section-8c0f020094a44c6b858454ef91ab4edf}

Ebenenattribut. Gilt für `layer=0`, wenn `layer=comp`. Gegenseitig exklusiv mit `src=` und `textPs=` in derselben Ebene; Das letzte Vorkommen von `text=`, `textPs=` und `src=` hat Vorrang und stellt fest, ob es sich um ein Bild oder eine Textebene handelt. Von Effektebenen ignoriert.

## Standard {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Keine.

## Beispiel {#section-d011f765ec5c418d814a821019b0eef0}

Siehe die Beispiele in [Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) und [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-207b779ab67342a5acd343e6bcc749c4}

[Textformatierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [Textpositionierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
