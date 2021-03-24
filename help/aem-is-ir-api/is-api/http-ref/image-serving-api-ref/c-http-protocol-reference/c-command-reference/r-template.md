---
description: Erstellen einer Vorlage. Ermöglicht das Festlegen einer Compositing-Vorlage in einem anderen Katalog als dem Hauptkatalog.
solution: Experience Manager
title: Vorlage
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 6%

---


# Vorlage{#template}

Erstellen einer Vorlage. Hiermit können Sie eine Compositing-Vorlage in einem anderen Katalog als dem Hauptkatalog angeben.

`template= *`Vorlage`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Objekt</span> </p> </td> 
  <td class="stentry"> <p>Vorlage. </p></td> 
 </tr> 
</table>

*`template`* muss ein Bildkatalogeintrag mit dem Vorlagentext in  `catalog::Modifier`sein.

Wenn `template=` vorhanden ist, wird das im Anforderungspfad angegebene Objekt nicht als Quelle für Ebene 0 angewendet. Sie kann jedoch an einer beliebigen Stelle in der Vorlage als `src=` oder `mask=` referenziert werden, indem die vordefinierte Pfadvariable `$object$` als `src=`-Wert verwendet wird. `catalog::Modifier` des im Anforderungspfad angegebenen Objekts wird nur mit der Ersetzung durch  `$object$` die Vorlage angewendet, während  `catalog::PostModifier` es immer angewendet wird.

Ebene 0 ist im Vorlagenkörper definiert und kann eine Bild-, Farbton-, Text- oder verschachtelte oder eingebettete Anforderungsebene sein.

`catalog:PostModifier` von  *`object`* wird ignoriert, wenn  *`object`* mit verwendet  `template=`wird.

## Standard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Keine.

## Eigenschaften {#section-daf3afb1d09c45a6a394468d0874c439}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Beispiel {#section-9a4f260ed43342b186b0fe855f34bca6}

Siehe Beispiele unter [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-067587444f774469931ecafd5a39834c}

[Objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [vordefinierte Pfadvariable](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
