---
description: Verwenden Sie die folgenden Befehle für erweiterte Textformatierung.
solution: Experience Manager
title: Erweiterte Textformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Erweiterte Textformatierung{#advanced-text-formatting}

Verwenden Sie die folgenden Befehle für erweiterte Textformatierung.

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
   <td> <p>Position in Halbpunkten; Standard ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Hochgestellt ohne Änderung der Schriftgröße. </p> </td> 
   <td> <p>Position in Halbpunkten; Standard ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Deaktivieren/Aktivieren bei angegebener Schriftgröße. </p> </td> 
   <td> <p>Schriftgröße in Halbpunkten, oberhalb derer das Kerning angewendet werden soll; 0, um das Kerning zu deaktivieren; Standard ist 1, um alle Schriftgrößen über ½ Punkt zum Kerning zu bringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \KerningOptische </span> </td> 
   <td> <p>Optisches Kerning auswählen. </p> </td> 
   <td> <p> <span class="codeph"> textPs= nur </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \KerningMetric </span> </td> 
   <td> <p>Metrik-Kerning auswählen. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Expand <span class="varname"> N </span> </span> </td> 
   <td> <p>Ändern des Zeichenabstands. </p> </td> 
   <td> <p>Positive oder negative Quartalspunkte; Standardwert ist 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Ändern des Zeichenabstands. </p> </td> 
   <td> <p>Positive oder negative Twips. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Horizontale Zeichenskalierung. </p> </td> 
   <td> <p>Positiver oder negativer Prozentsatz; Standardwert ist 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Vertikale Zeichenskalierung. </p> </td> 
   <td> <p>Positiver oder negativer Prozentsatz; Standardwert ist 100; Dynamic Media-Erweiterung. </p> <p> <span class="codeph"> \CharScaley </span> auch den Zeilenabstand skalieren, wenn er mit <span class="codeph"> text= </span> angewendet wird. <span class="codeph"> textPs= </span> behält den Zeilenabstand bei, unabhängig vom Umfang der vertikalen Zeichenskalierung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Wählen Sie den Zeichenfluss von links nach rechts aus. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Wählen Sie Rechts-nach-links-Zeichenfluss aus. </p> </td> 
   <td> <p> <span class="codeph"> text= nur </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Aktivieren Sie das Kopieren und Anpassen und legen Sie die größte zulässige Schriftgröße fest. </p> </td> 
   <td> <p>Schriftgröße in Halbpunkten; <span class="codeph"> textPs= nur </span>; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Maximale Einpassungslinien (weiche Begrenzung). </p> </td> 
   <td> <p>0 für keine Zeilenbegrenzung; <span class="codeph"> textPs= nur </span>; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Maximale Einpassungslinien (Abschneiden). </p> </td> 
   <td> <p> <span class="codeph"> textPs= nur </span>; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \BaselineDir <span class="varname"> N </span> </span> </td> 
   <td> <p>Ausrichtung der Zeichen. </p> </td> 
   <td> <p> <span class="codeph"> textPs= nur </span>; bei nicht-römischen Schriftarten ignoriert; wird ignoriert, wenn <span class="codeph"> \stextflow1-</span> nicht aktiv ist. </p> <p>0 vertikal (Standard). </p> <p>1 Im Uhrzeigersinn um 90 Grad gedreht. </p> </td> 
  </tr> 
 </tbody> 
</table>
