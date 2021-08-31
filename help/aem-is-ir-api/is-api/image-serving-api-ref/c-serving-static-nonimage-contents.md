---
description: Sie können Image Serving verwenden, um Nicht-Bild-Inhalte in Katalogen zu verwalten und über einen separaten /is/content-Kontext bereitzustellen.
solution: Experience Manager
title: Bereitstellen von statischen (Nicht-Bild-)Inhalten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Bereitstellen von statischen (Nicht-Bild-)Inhalten{#serving-static-non-image-contents}

Sie können Image Serving verwenden, um Nicht-Bild-Inhalte in Katalogen zu verwalten und über einen separaten /is/content-Kontext bereitzustellen.

Diese Funktion ermöglicht die separate Konfiguration der TTL für jedes Element.

Image Serving unterstützt die folgenden Befehle unter [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Inhaltstypfilter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>und  <span class="codeph"> req=exists  </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache  </a> </p> </td> 
  <td class="stentry"> <p>Ermöglicht das Deaktivieren der clientseitigen Zwischenspeicherung. </p> </td> 
 </tr> 
</table>

## Basissyntax {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Anfrage  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item  </span>][? <span class="varname"> modifiers  </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ :  <span class="varname"> port  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Katalog  </span> </span> </p> </td> 
  <td class="stentry"> <p>Katalogkennung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>Kennung des statischen Inhaltselements. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifiers  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span>*[&amp;  <span class="varname"> command  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>Einer der unterstützten Befehlsnamen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Befehlswert. </p> </td> 
 </tr> 
</table>

## Statische Inhaltskataloge {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Statische Inhaltskataloge ähneln Bildkatalogen, unterstützen jedoch weniger Datenfelder:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut/Daten </p> </th> 
   <th colname="col2" class="entry"> <p>Anmerkungen </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
   <td colname="col2"> <p>Die Katalogdatensatzkennung für dieses statische Inhaltselement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path  </span> </p> </td> 
   <td colname="col2"> <p>Der Dateipfad für dieses Inhaltselement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration  </span> </p> </td> 
   <td colname="col2"> <p>TTL für dieses Inhaltselement; <span class="codeph"> attribute::Expiration </span> wird verwendet, wenn kein Wert angegeben oder leer ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Zeitstempel der Dateiänderung; erforderlich, wenn die Katalogbasierte Validierung mit dem Attribut <span class="codeph">::CacheValidationPolicy </span> aktiviert ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td colname="col2"> <p>Optionale Metadaten, die mit diesem statischen Inhaltselement verknüpft sind; verfügbar für den Client mit <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType  </span> </p> </td> 
   <td colname="col2"> <p>Optionaler Datentyp; kann verwendet werden, um Anforderungen nach statischen Inhalten mit dem Befehl <span class="codeph"> type= zu filtern.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtern von statischen Inhalten {#section-4c41bf41ff994910840c1352683d1f37}

Dieser Mechanismus kann dazu beitragen, dass Kunden nur Inhalte erhalten, die ihren Bedürfnissen entsprechen. Wenn der statische Inhalt mit geeigneten `catalog::UserType` -Werten getaggt wird, kann der Client den Befehl `type=` zur Anfrage hinzufügen. Image Serving vergleicht den mit dem Befehl `type=` bereitgestellten Wert mit dem Wert `catalog::UserType` und gibt im Fall einer Nichtübereinstimmung einen Fehler anstelle von möglicherweise ungeeigneten Inhalten zurück.

## Videountertiteldateien {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Sie können Videountertiteldateien (WebVTT), CSS oder beliebige Textdateien im JSONP-Format einschließen. Die JSON-Antwort wird unten beschrieben.

* Bei WebVTT-Dateien lautet der MIME-Typ der Antwort text/javascript. JSON wird nicht zurückgegeben; Stattdessen wird JavaScript zurückgegeben, das eine Methode mit JSON aufruft. Sowohl die ID als auch der Handler sind optional.
* Bei CSS-Dateien lautet der MIME-Typ der Antwort text/javascript. Sowohl die ID als auch der Handler sind optional.
* Standardmäßig wird die UTF-8-Kodierung angewendet, um sicherzustellen, dass sie korrekt dekodiert ist. Die standardmäßige Größenbeschränkung beträgt 2 MB.

Sie können auch Tracks für andere Arten zeitgesteuerter Metadaten verwenden. Die Quelldaten für jedes Verfolgungselement sind Textdateien, die aus einer Liste zeitgesteuerter Hinweise bestehen. Cues können Daten in Formaten wie JSON oder CSV enthalten.

Weitere Informationen zum JSONP-Format finden Sie unter [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) .

Weitere Informationen zum JSON-Format finden Sie unter [www.json.org](https://www.json.org) .

## Verwandte Themen {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Image Catalog Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
