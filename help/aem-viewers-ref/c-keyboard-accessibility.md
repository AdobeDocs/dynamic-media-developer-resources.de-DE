---
title: Tastaturzugriff und Navigation
description: Alle Funktionen, die in den Vieweroberflächen „Basic Zoom“, „eCatalog“, „eCatalog Search“, „Flyout“, „Inline Zoom“, „Mixed Media“, „Spin“, „Video“, „Zoom“, „Dimensional (3D)“, „Karussell“, „Interaktives Bild“, „Interaktives Video“ und „Video360“ verfügbar sind, können über die Tastatur aufgerufen werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Tastaturzugriff und Navigation{#keyboard-accessibility-and-navigation}

Alle Funktionen, die in den Vieweroberflächen „Basic Zoom“, „eCatalog“, „eCatalog Search“, „Flyout“, „Inline Zoom“, „Mixed Media“, „Spin“, „Video“, „Zoom“, „Carousel“, „Dimensional“ (3D)“, „Interaktives Bild“, „Interaktives Video“ und „Video360“ verfügbar sind, sind über die Tastatur zugänglich.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Tastaturzugriff und Navigation {#topic-f5650e9493404e55a3627c8d1366b861}

Alle Funktionen, die in den Vieweroberflächen „Basic Zoom“, „eCatalog“, „eCatalog Search“, „Flyout“, „Inline Zoom“, „Mixed Media“, „Spin“, „Video“, „Zoom“, „Carousel“, „Dimensional“ (3D)“, „Interaktives Bild“, „Interaktives Video“ und „Video360“ verfügbar sind, sind über die Tastatur zugänglich.

Ein Endbenutzer kann mit den Tastenkombinationen **[!UICONTROL Tab]** und **[!UICONTROL Umschalt+Tab]** zwischen Elementen der Viewer-Benutzeroberfläche navigieren. Mithilfe von **[!UICONTROL Tabulator]** wird der Eingabefokus auf das nächste Element der Benutzeroberfläche in der Tabulatorreihenfolge weitergeschaltet. Durch Verwendung von **[!UICONTROL Umschalt+Tab]** wird der Eingabefokus wieder auf das vorherige Element der Benutzeroberfläche zurückgesetzt. Die Fokusverschiebung folgt der natürlichen Position der Elemente der Benutzeroberfläche auf dem Bildschirm und bewegt sich in einer Reihenfolge von links nach rechts und dann von oben nach unten.

Je nach Betriebssystem und Webbrowser-Einstellungen erhält das Benutzeroberflächenelement mit Eingabefokus eine visuelle Fokusanzeige. Der visuelle Indikator kann beispielsweise ein dünner Rahmen sein, der um das Benutzeroberflächenelement gerendert wird.

Es ist möglich, diese Fokushervorhebung im Viewer-CSS zu deaktivieren oder anzupassen. Klicken Sie im Inhaltsverzeichnis dieses Hilfesystems unter einem bestimmten Viewer-Namen (z. B. Basic Zoom oder Interaktives Video) auf **Anpassen *Viewer*** >**&#x200B; Fokushervorhebung &#x200B;**.

Tastenkombinationen, die von einzelnen Elementen der Viewer-Benutzeroberfläche unterstützt werden, sind - in den meisten Fällen - offensichtlich und einfach zu entdecken.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Aktion </p> </th> 
   <th colname="col2" class="entry"> <p>Tastenanschlag </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aktivieren von Schaltflächenkomponenten </p> </td> 
   <td colname="col2"> <p>Leertaste oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vergrößern oder verkleinern </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> oder <span class="uicontrol"> - </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zurücksetzen des Zooms </p> </td> 
   <td colname="col2"> <p>Esc-Taste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schwenk </p> </td> 
   <td colname="col2"> <p>Nach oben, unten, links oder rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Drehen eines 360-Grad-Bildes </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Pfeiltasten, wenn sich das Bild im zurückgesetzten Zustand befindet. </p> <p>Verwenden Sie beim Arbeiten mit mehrdimensionalen Rotationssets die Pfeiltaste nach oben oder unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Auswahl von Produktmustern </p> </td> 
   <td colname="col2"> <p>Nach-oben-, Nach-unten-, Nach-links- oder Nach-rechts-Taste; Pos1- oder End-Taste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aktivierung von Produktmustern </p> </td> 
   <td colname="col2"> <p>Leertaste oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, schrittweises Zurückspulen </p> </td> 
   <td colname="col2"> <p>Nach-links- oder Nach-oben-Taste </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, schneller Vorlauf </p> </td> 
   <td colname="col2"> <p>Nach-rechts- oder Nach-unten-Taste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, zum Anfang oder Ende </p> </td> 
   <td colname="col2"> <p>Pos1- bzw. Pos1-Taste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und Interaktives Video, Lautstärkepegel steuern, wenn der Fokus auf dem Schieberegler liegt </p> </td> 
   <td colname="col2"> <p>Nach-oben-, Nach-unten-, Nach-links- oder Nach-rechts-Taste; Pos1- oder End-Taste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video und interaktives Video, veränderliche Lautstärke </p> </td> 
   <td colname="col2"> <p>Mit den Tasten Pfeil, Pos1 und Ende können Sie die Lautstärke regulieren, wenn der Fokus auf dem Schieberegler liegt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video: Wenn das modale Dialogfeld angezeigt wird, wird das Durchlaufen des Fokus auf Dialogfeldsteuerelemente beschränkt. </p> </td> 
   <td colname="col2"> <p>Esc-Taste zum Schließen des Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Karussell, Bannerbild in Hauptansicht ändern </p> </td> 
   <td colname="col2"> <p>Nach-links- oder Nach-rechts-Taste </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Karussell, Hotspot-Auswahl und Hotspot-Aktivierung </p> </td> 
   <td colname="col2"> <p>Hotspot-Auswahl: Pfeiltaste nach oben, unten, links oder rechts </p> <p>Hotspot-Aktivierung: Leertaste oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, Ändern des Seitenbilds in der Hauptansicht </p> </td> 
   <td colname="col2"> <p> Nach-links- oder Nach-rechts-Taste </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Katalog, Miniaturansicht auswählen </p> </td> 
   <td colname="col2"> <p>Pfeiltasten; Pos1 und Pos1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, Farbfeld-Aktivierung </p> </td> 
   <td colname="col2"> <p>Leertaste oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Katalog, Hotspot-Auswahl </p> </td> 
   <td colname="col2"> <p>Pfeiltasten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Katalog, Aktivierung </p> </td> 
   <td colname="col2"> <p>Leertaste oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Katalog, Aktivieren von Dropdown-Komponenten </p> </td> 
   <td colname="col2"> <p> Nach-unten-Taste; Leertaste oder Eingabetaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Katalog, wenn der Fokus im Dropdown-Bedienfeld ist </p> </td> 
   <td colname="col2"> <p>Wählen Sie mit den Pfeiltasten ein bestimmtes Element im Bedienfeld aus, bevor Sie es aktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bei der Anzeige eines modalen Dialogfelds in eCatalog wird der Fokusdurchlauf auf Dialogfeldsteuerelemente beschränkt. </p> </td> 
   <td colname="col2"> <p>Esc-Taste zum Schließen des Dialogfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>
