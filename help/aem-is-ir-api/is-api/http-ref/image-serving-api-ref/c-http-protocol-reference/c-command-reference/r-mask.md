---
title: mask
description: Bildmaske. Gibt ein separates Maskenbild an, das als nicht verknüpfte Maske verwendet werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# mask{#mask}

Bildmaske. Gibt ein separates Maskenbild an, das als nicht verknüpfte Maske verwendet werden soll.

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Objekt</span> </p></td> 
  <td class="stentry"> <p>Bildobjekt, das als Bild- oder Ebenenmaske verwendet werden soll. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Verschachtelte Image-Serving-, Bild-Rendering- oder externe Anforderung. </p></td> 
 </tr> 
</table>

*`object`* kann entweder ein Katalogeintrag oder eine Bild-/SVG-Datei sein. Kann für Bildebenen und einfarbige Ebenen angegeben werden.

Wenn *`object`* zu einem Bildkatalogeintrag aufgelöst wird, wird `catalog::MaskPath` verwendet oder, wenn `catalog::MaskPath` nicht definiert ist, wird `catalog::Path` verwendet. Wenn *`object`* nicht zu einem Katalogeintrag aufgelöst wird, wird dies als Dateipfad interpretiert.

Wenn das Quellbild in jedem Fall einen Alphakanal hat, wird es verwendet. Andernfalls wird das Bild bei Bedarf in Graustufen konvertiert, bevor es als Ebenenmaske verwendet wird.

Wenn eine Maske an eine einfarbige Ebene angehängt ist, kann sie mithilfe derselben Regeln, die für Bilder in Bildebenen verwendet werden, beschnitten und skaliert werden. `size=`, `scale=` oder `res=` können verwendet werden, um die Maske zu skalieren.

Ebenenmasken können auch in Form von *`nestedRequest`* angegeben werden. Verschachtelte oder eingebettete Anforderungen werden durch geschweifte Klammern eingeschlossen. Setzen Sie einer eingebetteten Image Serving-Anforderung den Wert `is` und einer eingebetteten Image Rendering-Anforderung den Wert `ir` voran. Wenn kein Präfix angegeben ist, wird eine Anfrage an einen Fremdserver angenommen. Weitere Informationen finden Sie unter [Verschachtelung und Einbettung anfordern](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) .

## Eigenschaften {#section-a093043dc249423b8ae322cefb0d545d}

Bild- oder Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. Wird von Effektebenen ignoriert.

*`object`* darf nicht in einen Katalogdatensatz aufgelöst werden, der einen `src=` - oder `mask=` -Befehl in `catalog::Modifier` enthält.

Bei den Präfixen `is` und `ir` wird nicht zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-10cf793c665f49deb1b248faa3b618a9}

Wenn `mask=` nicht explizit angegeben ist und das Ebenenbild mit einem Katalogeintrag verknüpft ist, wird `catalog::MaskPath` verwendet. Andernfalls wird der Alphakanal des Ebenenbilds verwendet, sofern vorhanden. Wenn kein Alphakanal vorhanden ist, hat die Ebene keine Maske und das Ebenenrechteck wird vollständig deckend dargestellt.

## Beispiel {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Verwenden Sie mehrere separate Masken, um verschiedene Bereiche eines Bildes zu färben. Die gefärbten, maskierten Bereiche werden auf dem ursprünglichen, unveränderten Bild überlagert:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Verwandte Themen {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Verschachtelung und Einbettung anfordern](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
