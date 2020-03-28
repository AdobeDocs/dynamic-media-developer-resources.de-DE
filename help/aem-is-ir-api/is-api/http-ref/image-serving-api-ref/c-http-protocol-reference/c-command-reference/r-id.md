---
description: Bild-/Metadatenversion. Bei der Arbeit mit häufig wechselnden Inhalten können Server in Cache-Netzwerken wie Akamai, Browser-Caches und Unternehmensproxy-Server-Caches Image Serving-Antworten speichern, die über längere Zeit veraltet sein können.
seo-description: Bild-/Metadatenversion. Bei der Arbeit mit häufig wechselnden Inhalten können Server in Cache-Netzwerken wie Akamai, Browser-Caches und Unternehmensproxy-Server-Caches Image Serving-Antworten speichern, die über längere Zeit veraltet sein können.
seo-title: id
solution: Experience Manager
title: id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# id{#id}

Bild-/Metadatenversion. Bei der Arbeit mit häufig wechselnden Inhalten können Server in Cache-Netzwerken wie Akamai, Browser-Caches und Unternehmensproxy-Server-Caches Image Serving-Antworten speichern, die über längere Zeit veraltet sein können.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span></span> </p> </td> 
  <td class="stentry"> <p>Versionszeichenfolge. </p> </td> 
 </tr> 
</table>

Image Serving enthält einen Versionsverwaltungsmechanismus, der dazu beitragen kann, die Wahrscheinlichkeit zu verringern, dass eine Anwendung einen veralteten Cache-Eintrag verwendet. Dieser Mechanismus umfasst die Verwendung `req=props` zum Abrufen von Versionskennzeichenfolgen für Bilddaten und Metadaten (z. B. Imagemap- oder Zoomdaten). Die Zeichenfolge für die Versionskennung wird dann mit dem `id=` Befehl zu den Cache-fähigen Image-Server-Anforderungen hinzugefügt.

Wenn sich ein Quellbild oder Metadaten ändert, ändert sich auch der entsprechende Wert für die Version-ID. Durch die Einbeziehung eines aktuellen Version-ID-Werts mit dem `id=` Befehl wird sichergestellt, dass kein Zugriff mehr auf alte Cache-Einträge möglich ist.

In der folgenden Tabelle sind die für jeden `req=` Typ zu verwendenden Versionskennzeichenfolgen Liste:

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

`req=` Typen, die oben nicht aufgeführt sind, haben entweder eine kurze TTL ( `attribute::NonImgExpiration`) oder ihre Antworten sind überhaupt nicht zwischengespeichert. Es gibt keinen Vorteil, solche Anfragen `id=` mit einzubeziehen.

## Eigenschaften {#section-62e973d0d5884abebbb0679f9278ae2c}

Anforderungsattribut. Optional. Wird immer vom Server ignoriert.

## Standard {#section-96136720c82842c89505347ec39e6024}

Keine.

## Beispiel {#section-a5fb871e0ec8485c91c4fca78895d17f}

Siehe die Beschreibung von [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) zum Beispiel Verwendung.

## Siehe auch {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
