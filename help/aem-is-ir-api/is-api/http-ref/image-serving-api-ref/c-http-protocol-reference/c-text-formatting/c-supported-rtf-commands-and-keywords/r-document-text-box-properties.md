---
description: Die folgenden Dokumenteigenschaften werden in Textfeldern unterstützt.
solution: Experience Manager
title: Eigenschaften des Dokuments (Textfeld)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Eigenschaften des Dokuments (Textfeld){#document-text-box-properties}

Die folgenden Dokumenteigenschaften werden in Textfeldern unterstützt.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Befehl</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
   <th class="entry"> <b>Hinweise</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Schriftartentabelle. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Zeichensatz für Schriftart <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ColorTbl </span> </td> 
   <td> <p>RGB-Farbtabelle. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \CMYKCOLORTBL </span> </td> 
   <td> <p>CMYK-Farbtabelle. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\isColorTbl-</span> </td> 
   <td> <p>Farbtabelle für Bildbereitstellungsfarben. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; nur <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Rote Farbkomponente. </p> </td> 
   <td> <p>Darf nur in <span class="codeph"> \colortbl </span>; 0…255 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \grün <span class="varname"> N </span> </span> </td> 
   <td> <p>Grüne Farbkomponente. </p> </td> 
   <td> <p>Darf nur in <span class="codeph"> \colortbl </span>; 0…255 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blau <span class="varname"> N </span> </span> </td> 
   <td> <p>Blaue Farbkomponente. </p> </td> 
   <td> <p>Darf nur in <span class="codeph"> \colortbl </span>; 0…255 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span> </span> </td> 
   <td> <p>Cyan-Farbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; darf nur in <span class="codeph"> \CMYKColortBL </span>; 0…100 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Magentafarbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; darf nur in <span class="codeph"> \CMYKColortBL </span>; 0…100 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Yellow <span class="varname"> N </span> </span> </td> 
   <td> <p>Gelbe Farbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; darf nur in <span class="codeph"> \CMYKColortBL </span>; 0…100 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \schwarz <span class="varname"> N </span> </span> </td> 
   <td> <p>Schwarzfarbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; darf nur in <span class="codeph"> \CMYKColortBL </span>; 0…100 angezeigt werden </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Linker Rand. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>Rechter Rand. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Oberer Rand. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margin <span class="varname"> n </span> </span> </td> 
   <td> <p>Unterer Rand. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= nur </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>Text im Textfeld nach oben ausrichten. </p> </td> 
   <td> <p>Standard </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>Text in Textfeld an der Unterseite ausrichten. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>Text im Textfeld zentrieren. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Ausrichtung des Textflusses. </p> </td> 
   <td> <p>Sprachspezifischer Textfluss; <span class="codeph"> textPs= </span> nur 0 (Standard) links-rechts, oben-unten (europäisch) 1 oben-unten, rechts-links (Fernost) </p> </td> 
  </tr> 
 </tbody> 
</table>
