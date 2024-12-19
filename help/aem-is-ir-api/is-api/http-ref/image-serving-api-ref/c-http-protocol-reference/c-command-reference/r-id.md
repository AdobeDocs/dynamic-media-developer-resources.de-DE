---
title: id
description: Bild-/Metadatenversion. Wenn Sie mit Inhalten arbeiten, die sich häufig ändern, können Server in Caching-Netzwerken wie Akamai, Browser-Caches und Unternehmens-Proxy-Server-Caches Bildbereitstellungsantworten speichern, die für Zeiträume veraltet sein können.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# id{#id}

Bild-/Metadatenversion. Wenn Sie mit Inhalten arbeiten, die sich häufig ändern, können Server in Caching-Netzwerken wie Akamai, Browser-Caches und Unternehmens-Proxy-Server-Caches Bildbereitstellungsantworten speichern, die für Zeiträume veraltet sein können.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Versionszeichenfolge. </p> </td> 
 </tr> 
</table>

Image Serving enthält einen Versionierungsmechanismus, mit dem die Wahrscheinlichkeit reduziert werden kann, dass ein veralteter Cache-Eintrag von einer Anwendung verwendet wird. Dieser Mechanismus umfasst die Verwendung von `req=props` zum Abrufen von Versionskennungszeichenfolgen für Bilddaten und Metadaten (z. B. Imagemap oder Zoom-Zieldaten). Die Versionskennungszeichenfolge wird dann mit dem `id=`-Befehl zu zwischenspeicherbaren Bildbereitstellungsanfragen hinzugefügt.

Wenn sich ein Quellbild oder Metadaten ändert, ändert sich auch der entsprechende Wert der Versions-ID. Durch die Verwendung eines aktuellen Versions-ID-Werts mit dem `id=`-Befehl wird sichergestellt, dass kein Zugriff mehr auf alte Cache-Einträge möglich ist.

In der folgenden Tabelle sind die für jeden `req=` zu verwendenden Versionskennungszeichenfolgen aufgeführt:

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
   <td> <p> Maske </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> als Target vorsehen </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> TMB </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> UserData </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> XMP </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` oben nicht aufgeführten Typen verfügen entweder über eine kurze TTL ( `attribute::NonImgExpiration`) oder ihre Antworten sind überhaupt nicht zwischenspeicherbar. Es hat keinen Vorteil, `id=` in solche Anfragen einzuschließen.

## Eigenschaften {#section-62e973d0d5884abebbb0679f9278ae2c}

Anforderungsattribut. Optional. Immer vom Server ignoriert.

## Standard {#section-96136720c82842c89505347ec39e6024}

Keine.

## Beispiel {#section-a5fb871e0ec8485c91c4fca78895d17f}

Siehe die Beschreibung von [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), zum Beispiel für die Verwendung.

## Siehe auch {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
