---
description: Standardbild für Antwort. Gibt das Bild oder den Katalogeintrag an, der verwendet werden soll, wenn ein Bild nicht gefunden werden kann.
seo-description: Standardbild für Antwort. Gibt das Bild oder den Katalogeintrag an, der verwendet werden soll, wenn ein Bild nicht gefunden werden kann.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---


# defaultImage{#defaultimage}

Standardbild für Antwort. Gibt das Bild oder den Katalogeintrag an, der verwendet werden soll, wenn ein Bild nicht gefunden werden kann.

` defaultImage= *`Objekt`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
</table>

*`object`* kann entweder ein Katalogeintrag (einschließlich einer Vorlage) oder ein einfacher Dateipfad sein. Nützlich zum Ersetzen fehlender Bilder durch Standardbilder. Dieser Wert überschreibt den Wert des entsprechenden Katalogs `attribute::DefaultImage`. Ein leerer Wert ( `defaultImage=`) deaktiviert die standardmäßige Bildbearbeitung.

>[!NOTE]
>
>Der Standard-Bildmechanismus gilt nicht für SVG-Objekte. Wenn das in der Anforderung angegebene SVG-Objekt nicht gefunden werden kann, wird ein Fehler zurückgegeben.

Wenn `attribute::DefaultImageMode=0`, *`object`* die gesamte ursprüngliche Anforderung ersetzt, auch wenn nur ein Bild in einer Komposition mit mehreren Bildern fehlt. Die einzigen Befehle, die von der ursprünglichen Anforderung beibehalten werden, sind: `wid=`, `hei=`, `fmt=`, `qlt=`.

Wenn `attribute::DefaultImageMode=1`, ersetzt das Objekt nur das fehlende Ebenenbild; Attribute für die fehlende Ebene werden angewendet und das Composite wird wie gewohnt verarbeitet und zurückgegeben.

## Eigenschaften {#section-d30923d8dc4042eba10989212dd70887}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn `req=` nicht `img` oder `tmb` ist.

## Einschränkungen {#section-30df31bc8cac41cd917f1e45196779c2}

Ausländische Bildquellen werden nicht durch den Standard-Bildmechanismus abgedeckt. Wenn eine ausländische Bildquelle nicht gültig ist, wird ein Fehler zurückgegeben.

Image Serving kehrt zurück zu `DefaultImageMode=0`, wenn verschachtelte Image Rendering- oder FXG-Renderanforderungen fehlschlagen.

## Standard {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Verwandte Themen {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [attribute: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
