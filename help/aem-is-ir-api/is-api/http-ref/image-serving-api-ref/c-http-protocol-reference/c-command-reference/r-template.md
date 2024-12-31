---
title: Vorlage
description: Compositing-Vorlage Ermöglicht die Angabe einer Zusammensetzungsvorlage, die sich in einem anderen Katalog als dem Hauptkatalog befindet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 4%

---

# Vorlage{#template}

Compositing-Vorlage Ermöglicht die Angabe einer Zusammensetzungsvorlage in einem anderen Katalog als dem Hauptkatalog.

`template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Objekt</span> </p> </td> 
  <td class="stentry"> <p>Vorlage. </p></td> 
 </tr> 
</table>

*`template`* muss ein Bildkatalogeintrag sein, wobei der Vorlagentext in `catalog::Modifier` enthalten sein muss.

Wenn `template=` vorhanden ist, wird das im Anfragepfad angegebene Objekt nicht als Quelle für Ebene 0 angewendet. Sie kann jedoch als `src=` oder `mask=` an einer beliebigen Stelle in der Vorlage referenziert werden, indem die vordefinierte PATH-Variable `$object$` als `src=` verwendet wird. `catalog::Modifier` des im Anfragepfad angegebenen Objekts wird nur mit der Ersetzung von `$object$` in der Vorlage angewendet, während `catalog::PostModifier` immer angewendet wird.

Ebene 0 wird im Vorlagentext definiert und kann ein Bild, eine Vollfarbe, ein Text oder eine verschachtelte oder eingebettete Anfrageebene sein.

`catalog:PostModifier` von *`object`* wird ignoriert, wenn *`object`* mit `template=` verwendet wird.

## Standard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Keine.

## Eigenschaften {#section-daf3afb1d09c45a6a394468d0874c439}

Anforderungsattribut. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet.

## Beispiel {#section-9a4f260ed43342b186b0fe855f34bca6}

Siehe Beispiele in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [predefined path variable](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
