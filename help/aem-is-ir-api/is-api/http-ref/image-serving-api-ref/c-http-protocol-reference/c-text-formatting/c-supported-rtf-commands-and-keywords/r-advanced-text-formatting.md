---
description: Verwenden Sie die folgenden Befehle für die erweiterte Textformatierung.
solution: Experience Manager
title: Erweiterte Textformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

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
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tiefgestellt ohne Änderung der Schriftgröße. </p> </td> 
   <td> <p>Position in Halbpunkten; Der Standardwert ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Hochgestellt ohne Änderung der Schriftgröße. </p> </td> 
   <td> <p>Position in Halbpunkten; Der Standardwert ist 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Deaktivieren/aktivieren Sie bei der angegebenen Schriftgröße. </p> </td> 
   <td> <p>Schriftgröße in Halbpunkten, über der das Kerning angewendet werden soll; 0 , um Kerning zu deaktivieren; Der Standardwert ist 1 für Kerning aller Schriftgrößen über ½ Punkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptische  </span> </td> 
   <td> <p>Wählen Sie optisches Kerning aus. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> nur. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>Wählen Sie Metrikkerning aus. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ändern Sie den Zeichenabstand. </p> </td> 
   <td> <p>positive oder negative Quartale; Der Standardwert ist 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ändern Sie den Zeichenabstand. </p> </td> 
   <td> <p>Positive oder negative Zweige. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Horizontale Zeichenskalierung. </p> </td> 
   <td> <p>Positiver oder negativer Prozentsatz; Der Standardwert ist 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Vertikale Zeichenskalierung. </p> </td> 
   <td> <p>Positiver oder negativer Prozentsatz; Standardwert ist 100; Dynamic Media-Erweiterung. </p> <p> <span class="codeph"> \charscaley skaliert  </span> auch den Zeilenabstand, wenn  <span class="codeph"> text= verwendet wird  </span>. <span class="codeph"> textPs= behält  </span> immer den Zeilenabstand bei, unabhängig von der Größe der vertikalen Zeichenskalierung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Wählen Sie den Zeichenfluss von links nach rechts aus. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Wählen Sie den Zeichenfluss von rechts nach links aus. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> nur. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Aktivieren Sie das Kopieren und legen Sie die maximal zulässige Schriftgröße fest. </p> </td> 
   <td> <p>Schriftgröße in Halbpunkten; <span class="codeph"> textPs= </span> nur; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximale Anzahl an Zeilen mit Copy-fit (weiche Begrenzung). </p> </td> 
   <td> <p>0 bei fehlender Zeilenbegrenzung; <span class="codeph"> textPs= </span> nur; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximale Anzahl an Zeilen mit Copy-Fit (Abschneiden). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Dynamic Media-Erweiterung. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Zeichenausrichtung. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; bei nichtrömischen Schriftarten ignoriert; ignoriert, wenn  <span class="codeph"> \stextflow1 nicht aktiv  </span> ist. </p> <p>0 vertikal (Standard). </p> <p>1 um 90 Grad im Uhrzeigersinn gedreht. </p> </td> 
  </tr> 
 </tbody> 
</table>
