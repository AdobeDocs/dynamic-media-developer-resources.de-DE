---
title: id
description: Bild-/Metadatenversion. Bei der Arbeit mit häufig wechselnden Inhalten speichern Server in Caching-Netzwerken wie Akamai, Browser-Caches und Unternehmens-Proxy-Server-Caches möglicherweise Image Serving-Antworten, die für einige Zeiträume veraltet sein können.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---

# id{#id}

Bild-/Metadatenversion. Bei der Arbeit mit häufig wechselnden Inhalten speichern Server in Caching-Netzwerken wie Akamai, Browser-Caches und Unternehmens-Proxy-Server-Caches möglicherweise Image Serving-Antworten, die für einige Zeiträume veraltet sein können.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Versionszeichenfolge. </p> </td> 
 </tr> 
</table>

Image Serving umfasst einen Versionierungsmechanismus, der dazu beitragen kann, die Wahrscheinlichkeit zu verringern, dass ein veralteter Cache-Eintrag von einer Anwendung verwendet wird. Dieser Mechanismus beinhaltet die Verwendung von `req=props` , um Zeichenfolgen zur Versionskennung für Bilddaten und Metadaten zu erhalten (z. B. Imagemap- oder Zoomzieldaten). Die Zeichenfolge der Versionskennung wird dann zu zwischenspeicherbaren Image Serving-Anforderungen mit der `id=` Befehl.

Wenn sich ein Quellbild oder Metadaten ändert, ändert sich auch der entsprechende Versions-ID-Wert. Einschließen eines aktuellen Versions-ID-Werts in die Variable `id=` -Befehl stellt sicher, dass nicht mehr auf alte Cache-Einträge zugegriffen wird.

In der folgenden Tabelle sind die Versionskennzeichenfolgen aufgeführt, die für die einzelnen `req=` Typ:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> Versionskennung von req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Karte </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mask </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> als Target vorsehen </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` Typen, die oben nicht aufgeführt sind, haben entweder eine kurze TTL ( `attribute::NonImgExpiration`) oder deren Antworten überhaupt nicht zwischenspeicherbar sind; es gibt keinen Vorteil, `id=` mit solchen Anfragen.

## Eigenschaften {#section-62e973d0d5884abebbb0679f9278ae2c}

Anforderungsattribut. Optional. Wird immer vom Server ignoriert.

## Standard {#section-96136720c82842c89505347ec39e6024}

Keine.

## Beispiel {#section-a5fb871e0ec8485c91c4fca78895d17f}

Siehe Beschreibung von [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) z. B. Verwendung.

## Siehe auch {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
