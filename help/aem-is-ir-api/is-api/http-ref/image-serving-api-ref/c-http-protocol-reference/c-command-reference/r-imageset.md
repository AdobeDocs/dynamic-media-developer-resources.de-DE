---
title: imageSet
description: Bildset. Gibt einen Bildset-Wert an, der beim Generieren einer req=set-Antwort verwendet werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# imageSet{#imageset}

Bildset. Gibt einen Bildset-Wert an, der beim Generieren einer req=set-Antwort verwendet werden soll.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildset-Zeichenfolge. </p></td> 
 </tr> 
</table>

Um den Wert mit Escape-Zeichen zu versehen und sicherzustellen, dass eingeschlossene Modifikatoren nicht als Teil der URL-Abfragezeichenfolge interpretiert werden, sollte der gesamte Wert in geschweifte Klammern eingeschlossen werden. Wenn der Katalogdatensatz im nächsten Pfad angegeben ist, überschreibt dieser Modifikatorwert `catalog::ImageSet` aus dem Hauptdatensatz. Eine Beschreibung der gültigen Bildset-Syntax finden Sie in `catalog::ImageSet` Dokumentation.

## Eigenschaften {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Anforderungsattribut. Optional. Überschreibt `catalog::ImageSet` aus dem Hauptdatensatz.

## Standard {#section-e8622ff40408450fb79d028f8d37fa6b}

Keine.

## Beispiel {#section-68513d3c601f477399602a0741dab390}

Geben Sie das Bildset für `req=set` Anfrage an:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Verwandte Themen {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Medienset-Anfragen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
