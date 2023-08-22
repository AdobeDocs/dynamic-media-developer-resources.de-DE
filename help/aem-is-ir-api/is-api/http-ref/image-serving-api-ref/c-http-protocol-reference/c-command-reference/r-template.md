---
title: Vorlage
description: Zusammenstellungsvorlage. Ermöglicht die Angabe einer Komponentenvorlage, die sich in einem anderen Katalog als dem Hauptkatalog befindet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# Vorlage{#template}

Zusammenstellungsvorlage. Hier können Sie eine Zusammenstellungsvorlage in einem anderen Katalog als dem Hauptkatalog angeben.

`template= *`Vorlage`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Objekt</span> </p> </td> 
  <td class="stentry"> <p>Vorlage. </p></td> 
 </tr> 
</table>

*`template`* muss ein Bildkatalogeintrag sein, wobei der Vorlagentext in `catalog::Modifier`.

Wann `template=` vorhanden ist, wird das im Anfragepfad angegebene Objekt nicht als Quelle für Ebene 0 angewendet. Sie kann jedoch als `src=` oder `mask=` an einer beliebigen Stelle in der Vorlage mithilfe der vordefinierten Pfadvariablen `$object$` as a `src=` -Wert. `catalog::Modifier` des im Anfragepfad angegebenen Objekts wird nur angewendet, wenn `$object$` in der Vorlage, während `catalog::PostModifier` immer angewendet wird.

Ebene 0 wird im Vorlagentext definiert und kann eine Bild-, Farbton-, Text- oder verschachtelte oder eingebettete Anfrageebene sein.

`catalog:PostModifier` von *`object`* wird ignoriert, wenn *`object`* wird mit `template=`.

## Standard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Keine.

## Eigenschaften {#section-daf3afb1d09c45a6a394468d0874c439}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Beispiel {#section-9a4f260ed43342b186b0fe855f34bca6}

Siehe Beispiele unter [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-067587444f774469931ecafd5a39834c}

[Objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Vordefinierte Pfadvariable](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
