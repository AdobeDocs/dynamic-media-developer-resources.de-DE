---
description: ID-Übersetzungszuordnung. Gibt die Regeln an, mit denen generische Bild-IDs in Gebietsschema-spezifische IDs übersetzt werden.
seo-description: ID-Übersetzungszuordnung. Gibt die Regeln an, mit denen generische Bild-IDs in Gebietsschema-spezifische IDs übersetzt werden.
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---


# LocaleMap{#localemap}

ID-Übersetzungszuordnung. Gibt die Regeln an, mit denen generische Bild-IDs in Gebietsschema-spezifische IDs übersetzt werden.

` *``*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Element</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>Gebietsschema-ID (nicht zwischen Groß- und Kleinschreibung unterscheiden) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Gebietsschema-Suffix. </p></td> 
 </tr> 
</table>

`LocaleMap` bezieht sich auf eine  `locId` Datei, die einer beliebigen Anzahl von zugeordnet werden kann  `locSuffix`.

Leere *`locSuffix`*-Werte sind zulässig. *`locSuffix`* Werte müssen in der Reihenfolge sortiert werden, in der sie gesucht werden sollen. Die erste Übereinstimmung wird zurückgegeben.

Image Serving sucht die *`locId`*-Werte nach einer Übereinstimmung, bei der die Groß-/Kleinschreibung nicht berücksichtigt wird, mit dem in der Anforderung angegebenen Wert. `locale=` Wenn eine Übereinstimmung gefunden wird, wird der erste zugehörige *`locSuffix`*-Wert an die ursprüngliche Katalog-ID angehängt. Wenn dieser Katalogeintrag vorhanden ist, wird er verwendet, andernfalls wird der nächste *`locSuffix`*-Wert versucht. Wenn keiner der *`locSuffix`*-Werte mit einem Katalogeintrag übereinstimmt, gibt Image Serving einen Fehler oder ein Standardbild zurück.

Ein leerer *`locId`*-Wert stimmt mit leeren und unbekannten `locale=`-Zeichenfolgen überein. Dadurch kann eine Standardregel für unbekannte Gebietsschemata definiert werden.

Wenn die ID-Übersetzung aktiviert ist, wird sie auf alle IDs angewendet, die auf Bildkatalog- und statische Inhaltskatalogeinträge verweisen.

## Eigenschaften {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Ein oder mehrere Elemente, durch |, wobei jedes Element aus zwei oder mehr durch Kommas getrennten Zeichenfolgenwerten besteht. *`locId`* und  `locale=` werden verglichen. Groß-/Kleinschreibung nicht beachten.

## Verwandte Themen {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Lokale Anpassung Support, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
