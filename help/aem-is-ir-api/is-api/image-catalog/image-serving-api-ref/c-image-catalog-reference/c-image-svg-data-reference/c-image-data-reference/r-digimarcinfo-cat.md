---
description: Digimarc-Bildinformationen. Aktiviert die Digimarc-Einbettung und gibt den Typ des Wasserzeichens und alle zugehörigen bildspezifischen Daten an.
seo-description: Digimarc-Bildinformationen. Aktiviert die Digimarc-Einbettung und gibt den Typ des Wasserzeichens und alle zugehörigen bildspezifischen Daten an.
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 12%

---


# DigimarcInfo{#digimarcinfo}

Digimarc-Bildinformationen. Aktiviert die Digimarc-Einbettung und gibt den Typ des Wasserzeichens und alle zugehörigen bildspezifischen Daten an.

## Eigenschaften {#section-62af219e8bac422b8541841221c9ce4f}

Vier Ganzzahlwerte, durch Kommas getrennt.

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*``*` typeenable Digimarc embedding and specify the watermark type:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>Wasserzeichentyp</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Basis. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Bild-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaktions-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Jahre des Urheberrechts. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`Ein `*` Bitfeld mit drei Werten wird markiert. Setzen Sie Bit 0 auf den Hinweis kopiergeschützter Inhalte, Bit 1 auf eingeschränkten Inhalt und Bit 2 auf erwachsenen Inhalt:

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> Flags</span> </span> </p> </th> 
   <th class="entry"> <p><b>Beschreibung</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Kopiergeschützt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Eingeschränkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Kopiergeschützt, eingeschränkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Reife Inhalte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Kopieren Sie geschützte Inhalte für Erwachsene. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Eingeschränkte Inhalte für Erwachsene. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Kopiergeschützter, eingeschränkter, ausgereifter Inhalt </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Interpretation von `*`val1`*` und `*`val2`*` hängt von `*`type`*` ab:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Bild-ID. </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Transaktions-ID. </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Erstes Jahr des Urheberrechts. </p> </td> 
   <td> <p>Zweites Urheberrechtsjahr. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Standard {#section-4bb97e5f79074be89cc691e73449eb43}

Von Attribut übernommen::DigimarcInfo, wenn das Feld nicht vorhanden oder leer ist.

## Beispiele {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot;deaktiviert die Digimarc-Wasserzeichen für dieses Bild.

&quot;1,5,0,0&quot;gibt ein einfaches Wasserzeichen mit dem Flag für jugendfreie und kopiergeschützte Inhalte an.

&quot;2,0,4567,0&quot;gibt ein Wasserzeichen mit einer Bild-ID an.

&quot;3,2,56483,0&quot;gibt ein Wasserzeichen mit einer Transaktions-ID und dem Kennzeichensatz für eingeschränkten Inhalt an.

&quot;4,0,1998,2001&quot; bezeichnet ein Wasserzeichen mit Urheberrechtsjahren.

## Verwandte Themen {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
