---
description: Anforderungsregelelement. Eine oder mehrere Regeln sind im Element <ruleSet> optional.
seo-description: Anforderungsregelelement. Eine oder mehrere Regeln sind im Element <ruleSet> optional.
seo-title: Regel
solution: Experience Manager
title: Regel
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 7%

---


# Regel{#rule}

Anforderungsregelelement. Eine oder mehrere Regeln sind im `<ruleset>`-Element optional.

## Attribute {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: Optional. Der Standardwert ist &quot;break&quot;.

`Replace = "first" | "all"`: Optional. Der Standardwert ist &quot;first&quot;.

`RequestType` =  *&quot;`types`&quot;*: Optional. Gibt an, für welchen Eingabekontext die Regel gilt. *`types`* ist eine kommagetrennte Liste, die eines oder mehrere der in der folgenden Tabelle aufgeführten Token enthalten kann. Wenn `RequestType` nicht angegeben ist, gilt die Regel für Anforderungen, die auf allen unterstützten Kontexten empfangen werden.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>Token</b> </p> </th> 
   <th class="entry"> <p><b>Kontext</b> </p> </th> 
   <th class="entry"> <p><b>Beschreibung</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> ist</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Auf Image Serving-Anforderungen angewendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Auf Image Rendering-Anforderungen angewendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> statisch</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Auf statische Inhaltsanforderungen angewendet </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: Optional. Dient zur Identifizierung des Elements `<rule>` in Debugging-Protokollen und Fehlermeldungen.

`  *`Attribut`* ="value"`: Optional. `<rule>` -Elemente können eines der folgenden Attribute in jeder beliebigen Kombination definieren. Wenn die Regel angegeben wurde und eine Übereinstimmung erzielt wurde, überschreiben sie die entsprechenden Katalogattribute für diese Anforderung. Die Standardgrenze ist `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Attribut  </span> </b> </th> 
   <th class="entry"> <p>Entsprechendes Bildkatalogattribut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> attribute::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Ablauf</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> attribute::Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> attribute::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribute::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> attribute::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribute::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> attribute::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> attribute::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen finden Sie in der Beschreibung des entsprechenden Attributs für den Bildkatalog.

Die Ablaufattribute setzen nur die Standardattributwerte außer Kraft. Die Außerkraftsetzung wird ignoriert, wenn ein bestimmter `catalog::Expiration`-Wert für die Anforderung gilt.

## Daten {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>Optional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>optional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>optional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;Header&gt;</span> </p></td> 
  <td class="stentry"> <p>optional </p></td> 
 </tr> 
</table>

## Anmerkungen {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Wenn sowohl `<expression>` als auch `<substitution>` angegeben sind und keine erfassten Unterzeichenfolgen verwendet werden, wird die erste übereinstimmende Unterzeichenfolge durch `<substitution>` ersetzt.

Wenn `<expression>` nicht angegeben ist, wird ein beliebiger Pfad übereinstimmen und `<substitution>` wird an das Ende des Pfades angehängt.

Wenn `<substitution>` nicht angegeben ist, findet keine Pfad- oder Abfrage-Transformation statt, jedoch werden alle angegebenen Katalogattribute überschrieben. Wenn `<substitution>` leer ist, wird die übereinstimmende Unterzeichenfolge entfernt.

`<addressfilter>` wird nur angewendet, wenn eine Übereinstimmung auftritt, und bevor Abfragen angewendet werden.
