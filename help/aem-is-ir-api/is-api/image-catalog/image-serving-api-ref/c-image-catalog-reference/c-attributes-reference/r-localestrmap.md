---
description: Zeichenfolgenübersetzungskarte. Bezieht sich auf eine locId, die einer beliebigen Anzahl von internalLocId zugeordnet werden kann.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# LocaleStrMap{#localestrmap}

Zeichenfolgenübersetzungskarte. Bezieht sich auf eine locId, die einer beliebigen Anzahl von internalLocId zugeordnet werden kann.

`*``*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Element </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Gebietsschema (nicht zwischen Groß- und Kleinschreibung unterscheiden) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>Interne Gebietsschema-ID. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` bezieht sich auf eine  `locId` , die einer beliebigen Anzahl von zugeordnet werden kann  `internalLocId`.

Ein leerer *`locale`* -Wert entspricht leeren und unbekannten `locale=` -Zeichenfolgen. Dadurch kann eine Standardregel für unbekannte Gebietsschemata definiert werden.

Leere *`locId`* -Werte sind zulässig und wählen Sie *`defaultString`* aus (das *`defaultString`* hat keine Gebietsschema-Kennung). *`locId`* -Werte in der angegebenen Reihenfolge durchsucht werden. Die erste Übereinstimmung wird zurückgegeben.

Wenn die Zeichenfolgenübersetzung aktiviert ist, wird sie auf Textzeichenfolgen in den folgenden Bildkatalogfeldern angewendet:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Katalogfeld</b> </td> 
   <td> <b>Zeichenfolgenelement im Feld</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>Jedes Unterelement, das eine übersetzbare Zeichenfolge enthält (getrennt durch eine beliebige Kombination der Trennzeichen ',' ';' ':' und/oder den Beginn/das Ende des Felds). </p> <p>Ein <span class="codeph"> 0xrggbb </span>-Farbwert am Anfang eines lokalisierbaren Felds wird aus der Lokalisierung ausgeschlossen und ohne Änderung weitergegeben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::Map  </span> </p> </td> 
   <td> <p>Ein- oder zweifacher Attributwert, ausgenommen die Werte der Attribute <span class="codeph"> coords= </span> und <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog:Targets  </span> </p> </td> 
   <td> <p>Der Wert eines beliebigen <span class="filepath">-Ziels.*.label </span> und <span class="filepath"> target.*.userdata </span> -Eigenschaft. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>Der -Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8505a8525f6948ada3979f68c4081044}

Ein oder mehrere Elemente, getrennt durch |, wobei jedes Element aus zwei oder mehr, kommagetrennten Zeichenfolgenwerten besteht.

## Verwandte Themen {#section-0c0516e4f83d42d38247308cab9b6708}

Lokalisierungsunterstützung, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData 11/>](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
