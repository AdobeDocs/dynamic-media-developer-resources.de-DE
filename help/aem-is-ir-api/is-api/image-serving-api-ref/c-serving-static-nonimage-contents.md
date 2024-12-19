---
title: Statische Inhalte (keine Bilder) bereitstellen
description: Sie können die Bildbereitstellung verwenden, um Nicht-Bildinhalte in Katalogen zu verwalten und über einen separaten /is/content-Kontext bereitzustellen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Statische Inhalte (keine Bilder) bereitstellen{#serving-static-non-image-contents}

Sie können die Bildbereitstellung verwenden, um Nicht-Bildinhalte in Katalogen zu verwalten und über einen separaten /is/content-Kontext bereitzustellen.

Diese Funktion ermöglicht die Konfiguration der TTL für jedes Element separat.

Image Serving unterstützt die folgenden Befehle bei [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local">-</a> </p> </td> 
  <td class="stentry"> <p>Content-Typ-Filter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> und <span class="codeph"> req=existiert </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> Cache-</a> </p> </td> 
  <td class="stentry"> <p>Ermöglicht die Deaktivierung des Client-seitigen Caching. </p> </td> 
 </tr> 
</table>

## Grundlegende Syntax {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Anfrage </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname">-Modifikatoren </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> SERVER_ADDRESS </span>[ : <span class="varname"> Port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Katalog </span> </span> </p> </td> 
  <td class="stentry"> <p>Katalogkennung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Element </span> </span> </p> </td> 
  <td class="stentry"> <p>Statische Inhaltselement-ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Modifikatoren </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Befehl </span>*[&amp; <span class="varname"> Befehl </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Befehl </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> Wert </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Einer der unterstützten Befehlsnamen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Befehlswert. </p> </td> 
 </tr> 
</table>

## Kataloge mit statischen Inhalten {#section-91014f17f0d543d7aaf24539b2d7d4b9}

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
   <td colname="col1"> <p> <span class="codeph">::ID </span> </p> </td> 
   <td colname="col2"> <p>Die ID des Katalogdatensatzes für dieses statische Inhaltselement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">::Path </span> </p> </td> 
   <td colname="col2"> <p>Der Dateipfad für dieses Inhaltselement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">::Expiration </span> </p> </td> 
   <td colname="col2"> <p>Die TTL für dieses Inhaltselement; <span class="codeph"> Attribut::Expiration </span> wird verwendet, wenn sie nicht angegeben ist oder leer ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Zeitstempel der Dateiänderung; erforderlich, wenn die katalogbasierte Validierung mit <span class="codeph"> Attribut aktiviert ist::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">::UserData-</span> </p> </td> 
   <td colname="col2"> <p>Optionale Metadaten, die mit diesem statischen Inhaltselement verknüpft sind; für den Client mit <span class="codeph"> req=userdata-</span> verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">::UserType </span> </p> </td> 
   <td colname="col2"> <p>Optionaler Datentyp; kann zum Filtern von Anfragen nach statischen Inhalten mit der </span> <span class="codeph"> type= verwendet werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtern statischer Inhalte {#section-4c41bf41ff994910840c1352683d1f37}

Dieser Mechanismus kann dazu beitragen, dass Kunden nur Inhalte erhalten, die ihren Anforderungen entsprechen. Wenn der statische Inhalt mit entsprechenden `catalog::UserType`-Werten getaggt ist, kann der Client der Anfrage den `type=`-Befehl hinzufügen. Image Serving vergleicht den mit dem `type=`-Befehl bereitgestellten Wert mit dem Wert von `catalog::UserType` und gibt bei einer Nichtübereinstimmung einen Fehler anstelle möglicherweise unangemessener Inhalte zurück.

## Videountertiteldateien {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Sie können Videountertiteldateien (WebVTT), CSS oder eine beliebige Textdatei im JSONP-Format kapseln. Die JSON-Antwort wird unten beschrieben.

* Bei WebVTT-Dateien lautet der MIME-Typ der Antwort text/javascript. JSON wird nicht zurückgegeben. Stattdessen wird JavaScript zurückgegeben, das eine Methode mit JSON aufruft. Sowohl die ID als auch der Handler sind optional.
* Bei CSS-Dateien lautet der MIME-Typ der Antwort „text/javascript“. Sowohl die ID als auch der Handler sind optional.
* Standardmäßig wird UTF-8-Codierung angewendet, um sicherzustellen, dass sie korrekt decodiert ist. Die standardmäßige Größenbeschränkung beträgt 2 MB.

Sie können auch Tracks für andere Arten von zeitgesteuerten Metadaten verwenden. Die Quelldaten für jedes Spurelement sind eine Textdatei, die aus einer Liste von zeitlich begrenzten Hinweisen besteht. Hinweise können Daten in Formaten wie JSON oder CSV enthalten.

Weitere Informationen zum JSONP-](https://en.wikipedia.org/wiki/JSONP) finden Sie unter [https://en.wikipedia.org/wiki/JSONP.

Weitere Informationen zum JSON-](https://www.json.org/json-en.html) finden Sie unter [www.json.org.

## Verwandte Themen {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Image Catalog Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
