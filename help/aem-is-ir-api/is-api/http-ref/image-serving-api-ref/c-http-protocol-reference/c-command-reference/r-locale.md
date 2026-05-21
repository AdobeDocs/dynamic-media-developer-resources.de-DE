---
title: standort
description: Übersetzungs-Gebietsschema-ID. Gibt die Gebietsschema-ID für die Anfrage an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
TQID: 'https://experienceleague.adobe.com/VTRopZpc1aMPvWk3QRd0XyAVf-y782AVidiSDiuYdKM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 4%

---

# standort{#locale}

Übersetzungs-Gebietsschema-ID. Gibt die Gebietsschema-ID für die Anfrage an.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>Gebietsschema-ID (Zeichenfolge). </p></td> 
 </tr> 
</table>

Unter Verwendung dieser ID und der mit `attribute::LocaleMap` und `attribute::LocaleStrMap` angegebenen Regeln wendet Image Serving die optionale Katalogübersetzung und Zeichenfolgen-Lokalisierung an.

## Eigenschaften {#section-1854a9902b884d9b8e8e713b6635723f}

Befehl anfordern. Gilt für die gesamte Anfrage, einschließlich verschachtelter/eingebetteter Anfragen, unabhängig davon, wo sie angegeben ist. `locId` dürfen nur druckbare ASCII-Zeichen enthalten. Diese Option wird ignoriert, wenn im Hauptkatalog dieser Anfrage keine Lokalisierungszuordnungen definiert sind. Ein Fehler wird zurückgegeben, wenn leere oder ungültige `locId` angegeben sind und keine Standardregel in `attribute::DefaultLocale` definiert ist.

## Standard {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` wird verwendet, wenn kein Gebietsschema= angegeben ist.

## Verwandte Themen {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Lokalisierungsunterstützung
