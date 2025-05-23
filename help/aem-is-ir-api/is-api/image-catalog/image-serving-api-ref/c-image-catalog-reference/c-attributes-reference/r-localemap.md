---
description: Übersetzungskarte der ID. Gibt die Regeln an, die für die Übersetzung generischer Bild-IDs in gebietsschemaspezifische IDs verwendet werden.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

Übersetzungskarte der ID. Gibt die Regeln an, die für die Übersetzung generischer Bild-IDs in gebietsschemaspezifische IDs verwendet werden.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Element</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>Gebietsschema-ID (nicht von Schreibweise abhängig). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Gebietsschema-Suffix. </p></td> 
 </tr> 
</table>

`LocaleMap` bezieht sich auf eine `locId`, die einer beliebigen Anzahl von `locSuffix` zugeordnet werden kann.

Leere *`locSuffix`* sind zulässig. *`locSuffix`* Werte müssen in der Reihenfolge sortiert werden, in der sie durchsucht werden sollen. Die erste Übereinstimmung wird zurückgegeben.

Die Bildbereitstellung durchsucht die *`locId`* nach einer Übereinstimmung, bei der nicht zwischen Groß- und Kleinschreibung unterschieden wird, mit dem in der Anfrage angegebenen `locale=`. Wenn eine Übereinstimmung gefunden wird, wird der erste verknüpfte *`locSuffix`* an die ursprüngliche Katalog-ID angehängt. Wenn dieser Katalogeintrag vorhanden ist, wird er verwendet, andernfalls wird der nächste *`locSuffix`* versucht. Wenn keiner der *`locSuffix`* Werte mit einem Katalogeintrag übereinstimmt, gibt Image Serving einen Fehler oder ein Standardbild zurück.

Ein leerer *`locId`* entspricht leeren und unbekannten `locale=`. Dies ermöglicht die Definition einer Standardregel für unbekannte Gebietsschemata.

Wenn die ID-Übersetzung aktiviert ist, wird sie auf alle IDs angewendet, die auf Bildkatalogeinträge und Katalogeinträge für statische Inhalte verweisen.

## Eigenschaften {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Ein oder mehrere Elemente, getrennt durch |, wobei jedes Element aus zwei oder mehr kommagetrennten Zeichenfolgenwerten besteht. *`locId`* und `locale=` werden verglichen. Groß-/Kleinschreibung wird nicht berücksichtigt.

## Verwandte Themen {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Lokalisierungsunterstützung, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
