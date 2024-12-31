---
title: DigimarcInfo
description: 'In: Digimarc image info. Aktiviert das Einbetten von Digimarc und legt den Typ des Wasserzeichens und alle zugehörigen bildspezifischen Daten fest.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---

# DigimarcInfo{#digimarcinfo}

In: Digimarc image info. Aktiviert das Einbetten von Digimarc und legt den Typ des Wasserzeichens und alle zugehörigen bildspezifischen Daten fest.

## Eigenschaften {#section-62af219e8bac422b8541841221c9ce4f}

Vier Ganzzahlwerte, durch Kommas getrennt.

`*`type`*, *`flags`*, *`val1`*, *`val2`*`

`*`type`*` aktiviert das Einbetten von Digimarc und gibt den Wasserzeichentyp an:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> Typ</span> </span> </p> </th> 
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
   <td> <p>Einfach. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Bild-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaktionskennung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4 </b> </p> </td> 
   <td> <p>Jahre des Urheberrechts. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`flags`*` ist ein Bit-Feld mit drei Werten. Setzen Sie Bit 0 auf kopiergeschützten Inhalt, Bit 1 auf eingeschränkten Inhalt und Bit 2 auf nicht jugendfreien Inhalt:

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
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Kopiergeschützt, eingeschränkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4 </b> </p> </td> 
   <td> <p>Reife Inhalte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5 </b> </p> </td> 
   <td> <p>Kopieren geschützter, nicht jugendfreier Inhalte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6 </b> </p> </td> 
   <td> <p>Eingeschränkte, für Erwachsene bestimmte Inhalte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7 </b> </p> </td> 
   <td> <p>Kopiergeschützte, eingeschränkte, reife Inhalte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Interpretation von `*`val1`*` und `*`val2`*` hängt von `*`type`*` ab:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> Typ</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> Val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> Val2 </span> </span> </p> </th> 
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
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaktionskennung. </p> </td> 
   <td> <p>Nicht verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4 </b> </p> </td> 
   <td> <p>Erstes Jahr des Urheberrechts. </p> </td> 
   <td> <p>Zweites Jahr des Urheberrechts. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Standard {#section-4bb97e5f79074be89cc691e73449eb43}

Von Attribut::DigimarcInfo geerbt, wenn das Feld nicht vorhanden oder leer ist.

## Beispiele {#section-0f14727a0a2a408781c9df71fed7f42d}

„0,0,0,0“ deaktiviert das Digimarc-Wasserzeichen für dieses Bild.

„1,5,0,0“ gibt ein einfaches Wasserzeichen mit dem Flag für Erwachsene und kopiergeschützte Inhalte an.

„2,0,4567,0“ gibt ein Wasserzeichen mit einer Bild-ID an.

„3,2,56483,0“ gibt ein Wasserzeichen mit einer Transaktions-ID und dem eingeschränkten Inhalts-Flag-Satz an.

„4,0,1998,2001“ gibt ein Wasserzeichen mit Copyright-Jahren an.

## Verwandte Themen {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
