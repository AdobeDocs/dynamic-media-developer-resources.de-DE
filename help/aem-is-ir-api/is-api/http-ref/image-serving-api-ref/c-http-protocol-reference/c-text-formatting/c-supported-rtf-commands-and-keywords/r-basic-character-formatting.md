---
description: Verwenden Sie die folgenden Befehle für die grundlegende Zeichenformatierung.
solution: Experience Manager
title: Grundlegende Zeichenformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d3bd6d4d-d7bd-4c9b-bc9e-7edaaac6378e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---

# Grundlegende Zeichenformatierung{#basic-character-formatting}

Verwenden Sie die folgenden Befehle für die grundlegende Zeichenformatierung.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> Befehl </th> 
   <th class="entry"> Beschreibung </th> 
   <th class="entry"> Anmerkungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \einfach </span> </td> 
   <td> <p>Die Zeichenformatierung auf den Standardwert zurücksetzen. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> nur. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Schriftbild. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl  </span> index. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Schriftgröße. </p> </td> 
   <td> <p>Halbpunkte; Der Standardwert ist 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Schriftfarbe. </p> </td> 
   <td> <p>0-basierter Index in Farbtabelle. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>Fettdruck. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>Kursiver Stil. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub  </span> </td> 
   <td> <p>Tiefgestellt. </p> </td> 
   <td> <p>Verkleinert die Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>Hochgestellt. </p> </td> 
   <td> <p>Verkleinert die Schriftgröße. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul  </span> </td> 
   <td> <p>Unterstreichen. </p> </td> 
   <td> <p>Image Serving erkennt außerdem die folgenden RTF-Unterstriche für Befehle: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld  </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash  </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd  </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb  </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth  </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw  </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave  </span> </li> 
     </ul> </p> <p>Diese werden zu diesem Zeitpunkt als Standard <span class="codeph"> \ul </span>-Unterstreichung implementiert. Alle anderen RTF-Unterstrichbefehle werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone  </span> </td> 
   <td> <p>Deaktivieren der Unterstreichung </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>Deaktivieren der Unterstreichung </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Großbuchstaben </span> </td> 
   <td> <p>großschreibung </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> nur. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>Kleinbuchstaben ("kleine Großbuchstaben") </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> nur. </p> </td> 
  </tr> 
 </tbody> 
</table>
