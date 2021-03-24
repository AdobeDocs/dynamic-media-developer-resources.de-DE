---
description: Bildsatz. Gibt einen Bildsatzwert an, der beim Generieren der Antwort "req=set"verwendet wird.
solution: Experience Manager
title: imageSet
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 8%

---


# imageSet{#imageset}

Bildsatz. Gibt einen Bildsatzwert an, der beim Generieren der Antwort &quot;req=set&quot;verwendet wird.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildsatzzeichenfolge. </p></td> 
 </tr> 
</table>

Um dem Wert zu entkommen und sicherzustellen, dass eingeschlossene Modifikatoren nicht als Teil der URL-Abfrage-Zeichenfolge interpretiert werden, sollte der gesamte Wert in geschweifte Klammern gesetzt werden. Wenn der Katalogdatensatz im Nettopfad angegeben ist, überschreibt dieser Modifikatorwert `catalog::ImageSet` aus dem Hauptdatensatz. Eine Beschreibung der gültigen Bildsatzsyntax finden Sie in der `catalog::ImageSet` Dokumentation.

## Eigenschaften {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Anforderungsattribut. Optional. Überschreibt `catalog::ImageSet` aus dem Hauptdatensatz.

## Standard {#section-e8622ff40408450fb79d028f8d37fa6b}

Keine.

## Beispiel {#section-68513d3c601f477399602a0741dab390}

Geben Sie den Bildsatz für die `req=set`-Anforderung an:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Verwandte Themen {#section-7e0320b2e09d475897082711a8f023a9}

[Katalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Medienset-Anforderungen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
