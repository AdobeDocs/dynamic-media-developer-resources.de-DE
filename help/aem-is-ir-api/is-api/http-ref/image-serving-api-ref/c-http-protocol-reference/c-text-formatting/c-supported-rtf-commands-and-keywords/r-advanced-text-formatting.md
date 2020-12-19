---
description: Verwenden Sie die folgenden Befehle zur erweiterten Textformatierung.
seo-description: Verwenden Sie die folgenden Befehle zur erweiterten Textformatierung.
seo-title: Erweiterte Textformatierung
solution: Experience Manager
title: Erweiterte Textformatierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# Erweiterte Textformatierung{#advanced-text-formatting}

Verwenden Sie die folgenden Befehle zur erweiterten Textformatierung.

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
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Skript ohne Änderung der Schriftgröße. </p> </td> 
   <td> <p>Position in Halbpunkten; der Standardwert ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Hochgestellt, ohne dass die Schriftgröße geändert wird. </p> </td> 
   <td> <p>Position in Halbpunkten; der Standardwert ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Deaktivieren/aktivieren bei angegebener Schriftgröße. </p> </td> 
   <td> <p>Schriftgröße in halben Punkten, oberhalb derer Kerning angewendet werden soll; 0 zur Deaktivierung des Kerning; Der Standardwert ist 1 für Kerning aller Schriftgrößen über ½ Punkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptischen  </span> </td> 
   <td> <p>Wählen Sie optisches Kerning. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> nur. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>Wählen Sie metrisches Kerning. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ändern Sie den Zeichenabstand. </p> </td> 
   <td> <p>positive oder negative Quartale-Punkte; der Standardwert ist 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ändern Sie den Zeichenabstand. </p> </td> 
   <td> <p>Positive oder negative Zweige. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Horizontale Zeichenskalierung. </p> </td> 
   <td> <p>positive oder negative Prozentsätze; der Standardwert ist 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Vertikale Zeichenskalierung. </p> </td> 
   <td> <p>positive oder negative Prozentsätze; default ist 100; Scene7-Erweiterung. </p> <p> <span class="codeph"> \charscaley skaliert  </span> auch den Zeilenabstand, wenn  <span class="codeph"> text= verwendet wird  </span>. <span class="codeph"> textPs= behält  </span> immer den Zeilenabstand unabhängig von der vertikalen Zeichenskalierung bei. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Wählen Sie den Textfluss von links nach rechts aus. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Wählen Sie den Zeichenfluss von rechts nach links aus. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> nur. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Aktivieren Sie die Kopiereinpassung und legen Sie die größtmögliche Schriftgröße fest. </p> </td> 
   <td> <p>Schriftgröße in halben Punkten; Nur <span class="codeph"> textPs= </span>; Scene7-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximal passende Linien (weiche Begrenzung). </p> </td> 
   <td> <p>0 für keine Zeilenbegrenzung; Nur <span class="codeph"> textPs= </span>; Scene7-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximal passende Linien (abschneiden). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Scene7-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zeichenausrichtung. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; bei nicht-lateinischen Schriften ignoriert; ignoriert, wenn  <span class="codeph"> \stextflow1 nicht aktiv  </span> ist. </p> <p>0 vertikal (Standard). </p> <p>1 um 90 Grad im Uhrzeigersinn gedreht. </p> </td> 
  </tr> 
 </tbody> 
</table>

