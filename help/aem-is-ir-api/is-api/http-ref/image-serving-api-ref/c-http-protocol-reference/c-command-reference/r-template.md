---
description: Erstellen einer Vorlage. Ermöglicht das Festlegen einer Compositing-Vorlage in einem anderen Katalog als dem Hauptkatalog.
seo-description: Erstellen einer Vorlage. Ermöglicht das Festlegen einer Compositing-Vorlage in einem anderen Katalog als dem Hauptkatalog.
seo-title: Vorlage
solution: Experience Manager
title: Vorlage
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 59b37d60-1d0c-4d0b-a5a0-98d8bf9e9064
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 6%

---


# Vorlage{#template}

Erstellen einer Vorlage. Ermöglicht das Festlegen einer Compositing-Vorlage in einem anderen Katalog als dem Hauptkatalog.

`template= *`Vorlage`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Objekt</span> </p> </td> 
  <td class="stentry"> <p>Vorlage. </p></td> 
 </tr> 
</table>

*`template`* muss ein Bildkatalogeintrag mit dem Vorlagentext in  `catalog::Modifier`sein.

Wenn `template=` vorhanden ist, wird das im Anforderungspfad angegebene Objekt nicht als Quelle für Ebene 0 angewendet, sondern kann mit der vordefinierten Pfadvariablen `$object$` als `src=`- oder `mask=`-Wert an einer beliebigen Stelle in der Vorlage referenziert werden. `src=` `catalog::Modifier` des im Anforderungspfad angegebenen Objekts wird nur in Verbindung mit der Ersetzung  `$object$` innerhalb der Vorlage angewendet, während  `catalog::PostModifier` dies immer angewendet wird.

Ebene 0 ist im Vorlagenkörper definiert und kann ein Bild, eine Volltonfarbe, Text oder eine verschachtelte oder eingebettete Anforderungsebene sein.

`catalog:PostModifier` von  *`object`* wird ignoriert, wenn  *`object`* mit verwendet  `template=`wird.

## Standard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Keine.

## Eigenschaften {#section-daf3afb1d09c45a6a394468d0874c439}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Beispiel {#section-9a4f260ed43342b186b0fe855f34bca6}

Siehe Beispiele unter [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-067587444f774469931ecafd5a39834c}

[Objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [vordefinierte Pfadvariable](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
