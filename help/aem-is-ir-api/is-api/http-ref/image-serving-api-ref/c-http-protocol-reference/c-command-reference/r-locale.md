---
description: Gebietsschema-ID der Übersetzung Gibt die Gebietsschema-ID für die Anforderung an.
solution: Experience Manager
title: standort
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---


# locale{#locale}

Gebietsschema-ID der Übersetzung Gibt die Gebietsschema-ID für die Anforderung an.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>Gebietsschema-ID (Zeichenfolge). </p></td> 
 </tr> 
</table>

Bei Verwendung dieser ID und der mit `attribute::LocaleMap` und `attribute::LocaleStrMap` angegebenen Regeln wendet Image Serving eine optionale Katalog-ID-Übersetzung und String-lokale Anpassung an.

## Eigenschaften {#section-1854a9902b884d9b8e8e713b6635723f}

Anforderungsbefehl. Gilt für die gesamte Anforderung, einschließlich verschachtelter/eingebetteter Anforderungen, unabhängig davon, wo sie angegeben wurde. `locId` darf nur druckbare ASCII-Zeichen enthalten. Wird ignoriert, wenn keine lokale Anpassung-Maps im Hauptkatalog dieser Anforderung definiert sind. Ein Fehler wird zurückgegeben, wenn ein leeres oder ungültiges `locId` angegeben ist und keine Standardregel in `attribute::DefaultLocale` definiert ist.

## Standard {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` wird verwendet, wenn locale= nicht angegeben ist.

## Verwandte Themen {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ,  [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),  [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Lokale Anpassung Support
