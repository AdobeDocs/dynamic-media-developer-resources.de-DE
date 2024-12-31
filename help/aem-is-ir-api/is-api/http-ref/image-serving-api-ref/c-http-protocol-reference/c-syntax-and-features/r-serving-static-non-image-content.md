---
description: Bereitstellen von statischem (Nicht-Bild-)Inhalt
solution: Experience Manager
title: Bereitstellen von statischem (Nicht-Bild-)Inhalt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Bereitstellen von statischem (Nicht-Bild-)Inhalt{#serving-static-non-image-content}

Die Bildbereitstellung bietet einen Mechanismus zum Verwalten von Nicht-Bildinhalten in Katalogen und deren Bereitstellung über eine separate `context /is/content`. Mit dem Mechanismus kann die TTL für jedes Element separat konfiguriert werden.

## Grundlegende Syntax {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Anfrage </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> catalog </span>/ <span class="varname"> item </span>][? <span class="varname">-Modifikatoren </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> SERVER_ADDRESS </span>[: <span class="varname"> Port </span>] </span> </p> </td> 
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

## Befehlsübersicht {#section-61657a0141914053ab12038ad7e91500}

Image-Serving unterstützt die folgenden Befehle unter /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local">-</a> </td> 
  <td class="stentry"> <p>Content-Typ-Filter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> und <span class="codeph"> req=existiert </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> Cache-</a> </td> 
  <td class="stentry"> <p>Ermöglicht die Deaktivierung des Client-seitigen Caching. </p> </td> 
 </tr> 
</table>

## Kataloge mit statischen Inhalten {#section-b2b8f4860fe84e528493ed704c7c5141}

Statische Inhaltskataloge ähneln Bildkatalogen, unterstützen jedoch weniger Datenfelder:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>/Daten</b> </th> 
   <th class="entry"> <b> Anmerkungen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::ID </span> </p> </td> 
   <td> <p> Die ID des Katalogdatensatzes für dieses statische Inhaltselement </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::Path </span> </p> </td> 
   <td> <p> Der Dateipfad für dieses Inhaltselement </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::Expiration </span> </p> </td> 
   <td> <p> Die TTL für dieses Inhaltselement; attribute::Expiration wird verwendet, wenn sie nicht angegeben ist oder leer ist </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::TimeStamp </span> </p> </td> 
   <td> <p> Zeitstempel der Dateiänderung; erforderlich, wenn die katalogbasierte Validierung mit dem Attribut aktiviert ist: CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::UserData-</span> </p> </td> 
   <td> <p> Optionale Metadaten, die mit diesem statischen Inhaltselement verknüpft sind; für den Client mit req=userdata verfügbar </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">::UserType </span> </p> </td> 
   <td> <p> Optionaler Datentyp; kann zum Filtern von Anfragen nach statischen Inhalten mit dem Befehl type= verwendet werden </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtern statischer Inhalte {#section-896c37cf68bc446eb0766fb378898262}

Dieser Mechanismus kann dazu beitragen, dass Kunden nur Inhalte erhalten, die ihren Anforderungen entsprechen. Wenn der statische Inhalt mit entsprechenden Tags (`catalog::UserType`) versehen ist, kann der Client der Anfrage den `type=`-Befehl hinzufügen. Image Serving vergleicht den mit dem `type=`-Befehl bereitgestellten Wert mit dem Wert von `catalog::UserType` und gibt bei einer Nichtübereinstimmung einen Fehler anstelle möglicherweise unangemessener Inhalte zurück.

## Verwandte Themen {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
