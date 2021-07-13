---
description: Alle Funktionen, die in der Benutzeroberfläche für den einfachen Zoom, E-Katalog, die E-Katalogsuche, Flyout, Inline-Zoom, gemischte Medien, Rotation, Video, Zoom, Dimensional (3D), Karussell, interaktives Bild, interaktives Video und Video360 verfügbar sind, sind über die Tastatur verfügbar.
solution: Experience Manager
title: Tastaturzugriff und Navigation
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Tastaturzugriff und Navigation{#keyboard-accessibility-and-navigation}

Alle Funktionen, die in der Benutzeroberfläche für den einfachen Zoom, E-Katalog, die E-Katalogsuche, Flyout, Inline-Zoom, gemischte Medien, Rotation, Video, Zoom, Karussell, Dimensional (3D), interaktive Bilder, interaktive Videos und Video360 verfügbar sind, sind über die Tastatur verfügbar.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Tastaturzugriff und Navigation {#topic-f5650e9493404e55a3627c8d1366b861}

Alle Funktionen, die in der Benutzeroberfläche für den einfachen Zoom, E-Katalog, die E-Katalogsuche, Flyout, Inline-Zoom, gemischte Medien, Rotation, Video, Zoom, Karussell, Dimensional (3D), interaktive Bilder, interaktive Videos und Video360 verfügbar sind, sind über die Tastatur verfügbar.

Ein Endbenutzer kann mithilfe der Tastenanschläge **[!UICONTROL Tab]** und **[!UICONTROL Umschalt+Tab]** zwischen Elementen der Viewer-Benutzeroberfläche navigieren. Durch Verwendung von **[!UICONTROL Tab]** wird der Eingabefokus auf das nächste Element der Benutzeroberfläche in der Tab-Reihenfolge weitergeleitet. Durch Verwendung von **[!UICONTROL Umschalt+Tab]** wird der Eingabefokus wieder auf das vorherige Element der Benutzeroberfläche zurückgesetzt. Das Fokus-Traversal folgt der natürlichen Elementposition der Benutzeroberfläche auf dem Bildschirm und bewegt sich von links nach rechts und dann von oben nach unten.

Je nach Betriebssystem und Webbrowsereinstellungen erhält das Element der Benutzeroberfläche mit Eingabefokus eine visuelle Fokusanzeige. Beispielsweise kann der visuelle Indikator ein dünner Rahmen sein, der um das Element der Benutzeroberfläche gerendert wird.

Es ist möglich, diese Fokushervorhebung im Viewer-CSS zu deaktivieren oder anzupassen. Klicken Sie im Inhaltsverzeichnis dieses Hilfesystems unter einem bestimmten Viewer-Namen (z. B. Basic Zoom or Interactive Video) auf **Anpassen *Name des Viewers*** >** Fokusmarkierung **.

Tastenanschläge, die von einzelnen Benutzeroberflächenelementen des Viewers unterstützt werden, sind in den meisten Fällen offensichtlich und leicht zu entdecken.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Aktion </p> </th> 
   <th colname="col2" class="entry"> <p>Keystroke </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Schaltflächenkomponenten aktivieren </p> </td> 
   <td colname="col2"> <p>Leerzeichen oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vergrößern oder Verkleinern </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> +  </span> oder  <span class="uicontrol"> -  </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom zurücksetzen </p> </td> 
   <td colname="col2"> <p>Esc-Schlüssel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bildschwenk </p> </td> 
   <td colname="col2"> <p>Nach oben, Nach unten, Nach-links oder Nach-rechts-Pfeiltaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Drehen eines 360-Grad-Bildes </p> </td> 
   <td colname="col2"> <p>Verwenden Sie Pfeiltasten, wenn das Bild zurückgesetzt ist. </p> <p>Verwenden Sie beim Arbeiten mit mehrdimensionalen Rotationssets die Nach-oben- oder Nach-unten-Pfeiltaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Auswahl von Produktmustern </p> </td> 
   <td colname="col2"> <p>Nach-oben-, Nach-unten-, Nach-links- oder Nach-rechts-Pfeiltaste; Home- oder End-Schlüssel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aktivierung von Produktmustern </p> </td> 
   <td colname="col2"> <p>Leerzeichen oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, stufenweise zurückspulen </p> </td> 
   <td colname="col2"> <p>Nach-links- oder Nach-oben-Pfeiltaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, schnell vorwärts </p> </td> 
   <td colname="col2"> <p>Pfeiltaste nach rechts oder unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, Anfang oder Ende </p> </td> 
   <td colname="col2"> <p>Home- bzw. End-Schlüssel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video: Steuern Sie die Lautstärke, wenn der Fokus auf den Regler liegt </p> </td> 
   <td colname="col2"> <p>Nach-oben-, Nach-unten-, Nach-links- oder Nach-rechts-Pfeiltaste; Home- oder End-Schlüssel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, veränderliche Lautstärke </p> </td> 
   <td colname="col2"> <p>Taste "Pfeil", "Startseite"und "Ende", um die Lautstärke zu steuern, wenn der Fokus auf den Regler gelegt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video: Wenn das modale Dialogfeld angezeigt wird, wird die Fokus-Umkehrung auf Dialogfeldsteuerelemente beschränkt. </p> </td> 
   <td colname="col2"> <p>Esc-Taste zum Schließen des Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Karussell, Bannerbild in der Hauptansicht ändern </p> </td> 
   <td colname="col2"> <p>Nach-links- oder Nach-rechts-Pfeiltaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Karussell, Hotspot-Auswahl und Hotspot-Aktivierung </p> </td> 
   <td colname="col2"> <p>Hotspot-Auswahl: Nach-oben-, Nach-unten-, Links- oder Nach-rechts-Pfeiltaste </p> <p>Hotspot-Aktivierung: Leerzeichen oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog das Seitenbild in der Hauptansicht ändern </p> </td> 
   <td colname="col2"> <p> Pfeiltasten nach links oder rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, Auswahl von Miniaturansichten </p> </td> 
   <td colname="col2"> <p>Pfeiltasten; Home- und End-Schlüssel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, Farbfeldaktivierung </p> </td> 
   <td colname="col2"> <p>Leerzeichen oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, Hotspot-Auswahl </p> </td> 
   <td colname="col2"> <p>Pfeiltasten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, Aktivierung </p> </td> 
   <td colname="col2"> <p>Leerzeichen oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog zur Aktivierung von Dropdown-Komponenten </p> </td> 
   <td colname="col2"> <p> Nach-unten-Pfeiltaste; Leerzeichen oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, wenn der Fokus im Dropdown-Bedienfeld liegt </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Pfeiltasten, um ein bestimmtes Element im Bedienfeld auszuwählen, bevor Sie es aktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog: Wenn ein modales Dialogfeld angezeigt wird, beschränkt sich die Fokus-Umkehrung auf Dialogfeldsteuerelemente. </p> </td> 
   <td colname="col2"> <p>Esc-Taste zum Schließen des Dialogfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>
