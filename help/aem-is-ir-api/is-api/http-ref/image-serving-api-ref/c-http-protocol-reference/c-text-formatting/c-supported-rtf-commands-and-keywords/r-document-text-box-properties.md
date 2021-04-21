---
description: Die folgenden Dokument-Eigenschaften werden in Textfeldern unterstützt.
solution: Experience Manager
title: Eigenschaften von Dokumenten (Textfeld)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Eigenschaften von Dokument (Textfeld){#document-text-box-properties}

Die folgenden Dokument-Eigenschaften werden in Textfeldern unterstützt.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Befehl</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
   <th class="entry"> <b>Anmerkungen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>Schriftarttabelle. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zeichensatz für Schrift <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>RGB-Farbtabelle. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK-Farbtabelle. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Farbtabelle für Image Serving-Farben. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; Nur <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rote Farbkomponente. </p> </td> 
   <td> <p>Darf nur in <span class="codeph"> \colortbl </span> angezeigt werden; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Grüne Farbkomponente. </p> </td> 
   <td> <p>Darf nur in <span class="codeph"> \colortbl </span> angezeigt werden; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Blaue Farbkomponente. </p> </td> 
   <td> <p>Darf nur in <span class="codeph"> \colortbl </span> angezeigt werden; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Cyan-Farbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; kann nur in <span class="codeph"> \cmykcolortbl </span> angezeigt werden; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Magenta-Farbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; kann nur in <span class="codeph"> \cmykcolortbl </span> angezeigt werden; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \gelb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Gelbe Farbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; kann nur in <span class="codeph"> \cmykcolortbl </span> angezeigt werden; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Schwarze Farbkomponente. </p> </td> 
   <td> <p>Dynamic Media-Erweiterung; kann nur in <span class="codeph"> \cmykcolortbl </span> angezeigt werden; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Linker Rand. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rechter Rand. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Oberer Rand. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Unterer Rand. </p> </td> 
   <td> <p>Twips; Nur <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Text im Textfeld oben ausrichten </p> </td> 
   <td> <p>Standard </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>Text im Textfeld unten ausrichten </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>Zentriert Text im Textfeld. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Textflussausrichtung </p> </td> 
   <td> <p>Sprachspezifischer Textfluss; <span class="codeph"> textPs= </span> nur 0 (Standard) links-rechts, oben-unten (europäisch) 1 oben-unten, rechts-links (Fertig-Osten) </p> </td> 
  </tr> 
 </tbody> 
</table>

