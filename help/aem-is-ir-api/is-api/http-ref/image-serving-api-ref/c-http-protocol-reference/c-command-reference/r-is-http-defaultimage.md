---
title: defaultImage
description: Standardbild für Antworten. Gibt den Bild- oder Katalogeintrag an, der verwendet werden soll, wenn ein Bild nicht gefunden werden kann.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

Standardbild für Antworten. Gibt den Bild- oder Katalogeintrag an, der verwendet werden soll, wenn ein Bild nicht gefunden werden kann.

` defaultImage= *`Objekt`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Objekt </span> </span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
</table>

*`object`* kann entweder ein Katalogeintrag (einschließlich einer Vorlage) oder ein einfacher Bilddateipfad sein. Nützlich zum Ersetzen fehlender Bilder durch Standardbilder. Dieser Wert überschreibt den Wert des entsprechenden Katalogs `attribute::DefaultImage`. Ein leerer Wert ( `defaultImage=`) deaktiviert die standardmäßige Bildverarbeitung.

>[!NOTE]
>
>Der standardmäßige Bildmechanismus gilt nicht für SVG-Objekte. Wenn das in der Anfrage angegebene SVG-Objekt nicht gefunden werden kann, wird ein Fehler zurückgegeben.

Wenn `attribute::DefaultImageMode=0`, ersetzt *`object`* die gesamte ursprüngliche Anforderung, selbst wenn nur ein Bild in einer Multibildkomposition fehlt. Die einzigen Befehle, die von der ursprünglichen Anforderung beibehalten werden, sind: `wid=`, `hei=`, `fmt=`, `qlt=`.

Wenn `attribute::DefaultImageMode=1`, ersetzt das Objekt nur das fehlende Ebenenbild. Attribute für die fehlende Ebene werden angewendet und der Verbund wird wie gewohnt verarbeitet und zurückgegeben.

## Eigenschaften {#section-d30923d8dc4042eba10989212dd70887}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Ignoriert, wenn `req=` nicht `img` oder `tmb` ist.

## Einschränkungen {#section-30df31bc8cac41cd917f1e45196779c2}

Ausländische Bildquellen werden vom standardmäßigen Bildmechanismus nicht abgedeckt. Wenn eine ausländische Bildquelle ungültig ist, wird ein Fehler zurückgegeben.

Beim Rendern verschachtelter Bilder oder bei FXG-Rendering-Anforderungen wird der Bildserver wieder auf &quot;`DefaultImageMode=0`&quot;zurückgesetzt.

## Standard {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Verwandte Themen {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
