---
description: Bildmaske. Gibt ein separates Maskenbild an, das als nicht verknüpfte Maske verwendet werden soll.
seo-description: Bildmaske. Gibt ein separates Maskenbild an, das als nicht verknüpfte Maske verwendet werden soll.
seo-title: Maske
solution: Experience Manager
title: Maske
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 1%

---


# mask{#mask}

Bildmaske. Gibt ein separates Maskenbild an, das als nicht verknüpfte Maske verwendet werden soll.

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Objekt</span> </p></td> 
  <td class="stentry"> <p>Bildobjekt, das als Bild- oder Ebenenmaske verwendet werden soll. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Verschachteltes Image Serving, Image Rendering oder externe Anforderung. </p></td> 
 </tr> 
</table>

*`object`* kann entweder ein Katalogeintrag oder eine Bild-/SVG-Datei sein. Kann für Bildebenen und Vollfarbebenen angegeben werden.

Wenn *`object`* zu einem Bildkatalogeintrag aufgelöst wird, `catalog::MaskPath` verwendet wird oder `catalog::MaskPath` nicht definiert ist, wird `catalog::Path` verwendet. Wenn *`object`* nicht in einen Katalogeintrag aufgelöst wird, wird dieser als Dateipfad interpretiert.

Wenn das Quellbild in jedem Fall einen Alpha-Kanal hat, wird es verwendet. Andernfalls wird das Bild bei Bedarf in Graustufen konvertiert, bevor es als Ebenenmaske verwendet wird.

Wenn eine Maske an eine Farbflächenebene angehängt wird, kann sie mit denselben Regeln wie für Bilder in Bildebenen beschnitten und skaliert werden. `size=`,  `scale=`oder  `res=` kann verwendet werden, um die Maske zu skalieren.

Ebenenmasken können auch in Form eines *`nestedRequest`* angegeben werden. Verschachtelte oder eingebettete Anforderungen werden durch geschweifte Klammern eingeschlossen. Präfix einer eingebetteten Image Serving-Anforderung mit `is` und einer eingebetteten Image Rendering-Anforderung mit `ir`. Eine Anforderung an einen Fremdserver wird angenommen, wenn kein Präfix angegeben ist. Weitere Informationen finden Sie unter [Verschachtelung und Einbettung anfordern](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Eigenschaften {#section-a093043dc249423b8ae322cefb0d545d}

Bild- oder Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. Von Effektebenen ignoriert.

*`object`* darf nicht in einen Katalogeintrag aufgelöst werden, der einen  `src=` oder einen  `mask=` Befehl enthält  `catalog::Modifier`.

Bei den Präfixen `is` und `ir` wird zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-10cf793c665f49deb1b248faa3b618a9}

Wenn `mask=` nicht explizit angegeben ist und das Ebenenbild mit einem Katalogeintrag verknüpft ist, wird `catalog::MaskPath` verwendet. Andernfalls wird, falls vorhanden, der Alpha-Kanal des Ebenenbilds verwendet. Wenn kein Alpha-Kanal vorhanden ist, hat die Ebene keine Maske und das Ebenenrechteck wird vollständig deckend dargestellt.

## Beispiel {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Verwenden Sie mehrere separate Masken, um verschiedene Bereiche eines Bildes zu färben. Die farbigen, maskierten Bereiche werden über dem ursprünglichen, unveränderten Bild angeordnet:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Verwandte Themen {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Request Verschachtelung und Einbettung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
