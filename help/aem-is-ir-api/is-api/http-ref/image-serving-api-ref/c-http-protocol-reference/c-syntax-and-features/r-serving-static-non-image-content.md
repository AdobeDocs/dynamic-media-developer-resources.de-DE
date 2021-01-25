---
description: Bereitstellen von statischen Inhalten (ohne Bilder)
solution: Experience Manager
title: Bereitstellen von statischen Inhalten (ohne Bilder)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4ec483fe-68a4-4ae2-b5ce-730229a9bc15
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Bereitstellen von statischem (Nicht-Bild-)Inhalt{#serving-static-non-image-content}

Image Serving bietet einen Mechanismus zum Verwalten von Nicht-Bild-Inhalten in Katalogen und deren Bereitstellung über ein separates `context /is/content`. Der Mechanismus ermöglicht die separate Konfiguration der TTL für jedes Element.

## Grundlegende Syntax {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anfordern  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http://  <span class="varname"> server  </span>/is/content[/  <span class="varname"> catalog  </span>/  <span class="varname"> item  </span>][? <span class="varname"> Modifikatoren  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[:  <span class="varname"> port  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Katalog  </span> </span> </p> </td> 
  <td class="stentry"> <p>Katalog-ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID des statischen Inhaltselements. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Modifikatoren  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span>*[&amp;  <span class="varname"> command  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> Wert  </span> </span> </p> </td> 
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

## Befehlsübersicht {#section-61657a0141914053ab12038ad7e91500}

Image Serving unterstützt die folgenden Befehle unter /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Inhaltstypfilter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req  </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>und  <span class="codeph"> req=exists  </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache  </a> </td> 
  <td class="stentry"> <p>Ermöglicht die Deaktivierung der clientseitigen Zwischenspeicherung. </p> </td> 
 </tr> 
</table>

## Statische Inhaltskataloge {#section-b2b8f4860fe84e528493ed704c7c5141}

Statische Inhaltskataloge sind ähnlich wie Bildkataloge, unterstützen jedoch weniger Datenfelder:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Daten</b> </th> 
   <th class="entry"> <b> Anmerkungen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::ID  </span> </p> </td> 
   <td> <p> Die Katalogdatensatzkennung für dieses statische Inhaltselement </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::Pfad  </span> </p> </td> 
   <td> <p> Der Dateipfad für dieses Inhaltselement </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::Ablauf  </span> </p> </td> 
   <td> <p> Die TTL für dieses Inhaltselement; attribute::Expiration wird verwendet, wenn nicht angegeben oder wenn leer </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::TimeStamp  </span> </p> </td> 
   <td> <p> Zeitstempel der Dateiänderung; erforderlich, wenn die katalogbasierte Validierung mit Attribut aktiviert ist::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::UserData  </span> </p> </td> 
   <td> <p> Optionale Metadaten, die mit diesem statischen Inhaltselement verknüpft sind; für den Client mit req=userdata verfügbar </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Katalog::UserType  </span> </p> </td> 
   <td> <p> Optionaler Datentyp; kann verwendet werden, um Anforderungen für statischen Inhalt mit dem Befehl type= zu filtern </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtern von statischem Inhalt {#section-896c37cf68bc446eb0766fb378898262}

Dieser Mechanismus kann dazu beitragen, dass Kunden nur Inhalte erhalten, die ihren Bedürfnissen entsprechen. Wenn der statische Inhalt mit entsprechenden `catalog::UserType`Werten versehen ist, kann der Client der Anforderung den Befehl `type=` hinzufügen. Image Serving vergleicht den mit dem Befehl `type=` bereitgestellten Wert mit dem Wert `catalog::UserType` und gibt im Falle einer Nichtübereinstimmung einen Fehler anstelle von potenziell unangemessenen Inhalten zurück.

## Verwandte Themen {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Bildkatalog-Referenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
