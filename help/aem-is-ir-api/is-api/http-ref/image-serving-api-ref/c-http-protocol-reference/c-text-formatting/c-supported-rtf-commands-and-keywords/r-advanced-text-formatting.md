---
description: Verwenden Sie die folgenden Befehle für die erweiterte Textformatierung.
solution: Experience Manager
title: Erweiterte Textformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Erweiterte Textformatierung{#advanced-text-formatting}

Verwenden Sie die folgenden Befehle für die erweiterte Textformatierung.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Befehl </th> 
   <th class="entry"> Beschreibung </th> 
   <th class="entry"> Anmerkungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> n </span> </span> </td> 
   <td> <p>Tiefgestellt ohne Änderung der Schriftgröße. </p> </td> 
   <td> <p>Position in Halbpunkten; Standardwert ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> n </span> </span> </td> 
   <td> <p>Hochgestellt ohne Änderung der Schriftgröße. </p> </td> 
   <td> <p>Position in Halbpunkten; Standardwert ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> n </span> </span> </td> 
   <td> <p>Deaktivieren/aktivieren Sie bei der angegebenen Schriftgröße. </p> </td> 
   <td> <p>Schriftgröße in halben Punkten, über der Kerning angewendet werden soll; 0 zum Deaktivieren des Kernings; der Standardwert ist 1 für Kerning aller Schriftgrößen über ½ Punkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptische </span> </td> 
   <td> <p>Wählen Sie optisches Kerning aus. </p> </td> 
   <td> <p> Nur <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Wählen Sie Metrikkerning aus. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expand <span class="varname"> n </span> </span> </td> 
   <td> <p>Ändern Sie den Zeichenabstand. </p> </td> 
   <td> <p>Positive oder negative Quartale; Standardwert ist 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> n </span> </span> </td> 
   <td> <p>Ändern Sie den Zeichenabstand. </p> </td> 
   <td> <p>Positive oder negative Zweige. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Horizontale Zeichenskalierung. </p> </td> 
   <td> <p>Positiver oder negativer Prozentsatz; Standardwert ist 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> n </span> </span> </td> 
   <td> <p>Vertikale Zeichenskalierung. </p> </td> 
   <td> <p>Positiver oder negativer Prozentsatz; Standardwert ist 100; Dynamic Media-Erweiterung. </p> <p> <span class="codeph"> \charscaley </span> skaliert auch den Zeilenabstand bei Anwendung von <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> behält den Zeilenabstand unabhängig von der vertikalen Zeichenskalierung bei. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Wählen Sie den Zeichenfluss von links nach rechts aus. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Wählen Sie den Zeichenfluss von rechts nach links aus. </p> </td> 
   <td> <p> Nur <span class="codeph"> text= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> n </span> </span> </td> 
   <td> <p>Aktivieren Sie das Kopieren und legen Sie die maximal zulässige Schriftgröße fest. </p> </td> 
   <td> <p>Schriftgröße in Halbpunkten; <span class="codeph"> textPs= </span> nur; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> n </span> </span> </td> 
   <td> <p>Maximale Anzahl an Zeilen mit Copy-fit (weiche Begrenzung). </p> </td> 
   <td> <p>0 für keine Zeilenbegrenzung; <span class="codeph"> textPs= </span> nur; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> n </span> </span> </td> 
   <td> <p>Maximale Anzahl an Zeilen mit Copy-Fit (Abschneiden). </p> </td> 
   <td> <p> Nur <span class="codeph"> textPs= </span>; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> n </span> </span> </td> 
   <td> <p>Zeichenausrichtung. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> nur; bei nicht-römischen Schriftarten ignoriert; wird ignoriert, wenn <span class="codeph"> \stextflow1 </span> nicht aktiv ist. </p> <p>0 vertikal (Standard). </p> <p>1 um 90 Grad im Uhrzeigersinn gedreht. </p> </td> 
  </tr> 
 </tbody> 
</table>
