---
title: src
description: Ebenenbild.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# src{#src}

Ebenenbild.

` src= *`object`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest-</span> </p> </td> 
  <td class="stentry"> <p>Bereitstellung verschachtelter Bilder, Image-Rendering oder externe Anforderung. </p> </td> 
 </tr> 
</table>

## Beschreibung {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Gibt das Quellbild für eine Bildebene an.

*`object`* kann entweder ein Katalogeintrag oder eine Bild-/SVG-Datei sein.

Siehe [Objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Verschachtelte oder eingebettete Anforderungen sind von geschweiften Klammern umgeben. Stellen Sie einer eingebetteten Bildbereitstellungsanfrage das Präfix &quot;`is`&quot;, einer eingebetteten Bildbereitstellungsanfrage das Präfix &quot;`ir`&quot; und einer FXG Graphics Render-Anfrage das Präfix &quot;`fxg`&quot; voran. Eine Anfrage an einen Fremdserver wird angenommen, wenn kein Präfix angegeben ist.

Siehe [Verschachtelung und Einbettung anfordern](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Eigenschaften {#section-2c22bb89a35d470f833df8ba898efd93}

Ebenenattribut. Gilt für `layer=0`, falls `layer=comp`. Sich gegenseitig ausschließend mit `text=` und `textPs=` in derselben Ebene, wobei das letzte Vorkommen von `text=`, `textPs=` oder `src=` vorherrscht und bestimmt, ob es sich um ein Bild oder eine Textebene handelt. Von Effektebenen ignoriert.

*`object`* kann nicht in einen anderen Katalogeintrag aufgelöst werden, der einen `src=`- oder `mask=`-Befehl in seiner `catalog::Modifier` enthält. (Verwenden Sie eine Anfragenverschachtelung, um einen ähnlichen Effekt zu erzielen.)

Bei den Präfixen für `is`, `ir` und `fxg` wird zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-a92f3882041b4d43ae2caf014647165f}

Für Ebene 0 wird das Objekt aus der Pfadkomponente der URL verwendet, wenn `src=` nicht angegeben ist. Kein Standardwert für andere Ebenen.

## Verwandte Themen {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
