---
description: Ebenenbild.
seo-description: Ebenenbild.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# src{#src}

Ebenenbild.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Objekt </span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Verschachteltes Image Serving, Image Rendering oder externe Anforderung. </p> </td> 
 </tr> 
</table>

## Beschreibung {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Gibt das Quellbild für eine Bildebene an.

*`object`* kann entweder ein Katalogeintrag oder eine Bild-/SVG-Datei sein.

Siehe [Objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Verschachtelte oder eingebettete Anforderungen werden durch geschweifte Klammern eingeschlossen. Präfix einer eingebetteten Image Serving-Anforderung mit `is`, einer eingebetteten Image Rendering-Anforderung mit `ir`und einer FXG-Grafikwiedergabeanforderung mit `fxg`. Eine Anforderung an einen Fremdserver wird angenommen, wenn kein Präfix angegeben ist.

Siehe [Verschachtelung und Einbettung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)anfordern.

>[!NOTE]
>
>Das Rendering von FXG-Grafiken ist nur in der von Scene7 gehosteten Umgebung verfügbar und erfordert möglicherweise zusätzliche Lizenzen. Weitere Informationen erhalten Sie vom Scene7-Support.

## Eigenschaften {#section-2c22bb89a35d470f833df8ba898efd93}

Ebenenattribut. Gilt für `layer=0` if `layer=comp`. Gegenseitig mit `text=` und in derselben Ebene `textPs=` ; das letzte Vorkommen entweder `text=`, `textPs=`oder `src=` siegt und bestimmt, ob es sich um ein Bild oder eine Textebene handelt. Von Effektebenen ignoriert.

*`object`*kann nicht zu einem anderen Katalogeintrag aufgelöst werden, der einen `src=` oder `mask=` Befehl in seinem enthält `catalog::Modifier`. (Verwenden Sie die Anforderungsverschachtelung, um einen ähnlichen Effekt zu erzielen.)

Bei den Präfixen `is`, `ir`und `fxg` wird zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-a92f3882041b4d43ae2caf014647165f}

Bei Ebene 0 wird das Objekt aus der Pfadkomponente der URL verwendet, wenn nicht angegeben `src=` ist. Kein Standardwert für andere Ebenen.

## Verwandte Themen {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[object,Templates,Request Verschachtelung und Einbettung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
