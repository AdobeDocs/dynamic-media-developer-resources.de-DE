---
description: Übersetzungszuordnung für Zeichenfolgen. Bezieht sich auf eine LocId, die einer beliebigen Anzahl von internalLocId zugeordnet werden kann.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

Übersetzungszuordnung für Zeichenfolgen. Bezieht sich auf eine LocId, die einer beliebigen Anzahl von internalLocId zugeordnet werden kann.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> <span class="varname"> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Gebietsschema (nicht von Schreibweise abhängig). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId-</span> </p> </td> 
  <td class="stentry"> <p>Interne Gebietsschema-ID. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` bezieht sich auf eine `locId`, die einer beliebigen Anzahl von `internalLocId` zugeordnet werden kann.

Ein leerer *`locale`* entspricht leeren und unbekannten `locale=`. Dies ermöglicht die Definition einer Standardregel für unbekannte Gebietsschemata.

Leere *`locId`* sind zulässig und wählen Sie die *`defaultString`* aus (der *`defaultString`* verfügt über keine Gebietsschema-Kennung). *`locId`* werden in der angegebenen Reihenfolge durchsucht. Die erste Übereinstimmung wird zurückgegeben.

Wenn die Zeichenfolgenübersetzung aktiviert ist, wird sie auf Textzeichenfolgen in den folgenden Bildkatalogfeldern angewendet:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Katalogfeld</b> </td> 
   <td> <b>Zeichenfolgenelement im Feld</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::ImageSet-</span> </p> </td> 
   <td> <p>Beliebiges Unterelement, das eine übersetzbare Zeichenfolge enthält (durch eine beliebige Kombination von Trennzeichen ',' ';' ':' und/oder den Anfang/das Ende des Felds getrennt). </p> <p>Ein <span class="codeph"> 0xrggbb </span> Farbwert am Anfang eines lokalisierbaren Felds wird von der Lokalisierung ausgeschlossen und unverändert weitergeleitet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::Map </span> </p> </td> 
   <td> <p>Jeder Attributwert in einfachen oder doppelten Anführungszeichen, mit Ausnahme der Werte der Attribute <span class="codeph"> = </span> und <span class="codeph"> Shape= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::Targets-</span> </p> </td> 
   <td> <p>Der Wert eines beliebigen <span class="filepath">.*.label </span> und <span class="filepath"> Target.*.UserData-</span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::UserData-</span> </p> </td> 
   <td> <p>Der Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8505a8525f6948ada3979f68c4081044}

Ein oder mehrere Elemente, getrennt durch |, wobei jedes Element aus zwei oder mehr durch Kommas getrennten Zeichenfolgenwerten besteht.

## Verwandte Themen {#section-0c0516e4f83d42d38247308cab9b6708}

Lokalisierungsunterstützung, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
