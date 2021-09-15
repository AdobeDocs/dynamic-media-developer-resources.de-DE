---
description: Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.
solution: Experience Manager
title: Kompatibilitätshinweise
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# Kompatibilitätshinweise{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Inkompatibilität mit älteren adaptiven Videosets Laden Sie adaptive Videosets erneut, um die Wiedergabe zu ermöglichen.

## Allgemein {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Die Browser-seitige Skalierung bewirkt, dass die Benutzeroberfläche und die Bilder beim Vergrößern der Seite durch den Benutzer verschwommen werden. Die Formatierung der Benutzeroberfläche wird je nach Zoom ebenfalls falsch angezeigt und wird auf den Vollbildmodus übertragen.
* Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien eine Foliengeste, um Frames in eingebetteten Bildsets zu tauschen, anstatt auf die eingebettete Farbfeldkomponente zu tippen. Die Komponente ist als visueller Indikator verfügbar.
* In Internet Explorer-Browsern und einigen Touch-Geräten nimmt der Vollbildmodus nicht den gesamten Gerätebildschirm ein. Stattdessen wird die Größe der Anwendung an die Größe des Browser-Fensters angepasst.
* Die Schaltfläche &quot;Schließen&quot;funktioniert unter iOS 8.0 und iOS 8.1 nicht, funktioniert aber unter iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Speicherleck bei Zoom- und eCatalog-Viewern. Die wiederholte Navigation durch Frames führt zum Absturz des Browsers.
* Durch Doppeltippen auf einen Viewer wird die gesamte Seite vergrößert, anstatt nur den Viewer mit aktivierter Browser-seitiger Skalierung anzuzeigen.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Gerät als Tablet im Hochformat erkannt, wobei Vollbild in den Browsereinstellungen aktiviert ist.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Durch Doppeltippen auf einen Viewer wird die gesamte Seite vergrößert und nicht nur der Viewer, wobei die Browser-seitige Skalierung aktiviert ist.

## Galaxy Nexus 10 und Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* Der E-Katalog zeigt eine falsche Seitenverteilung mit Hochformat- und Querformatausrichtung.

## HTC-Mobilgeräte {#section-dc42c80414c842e488738fc157c55b01}

* Die Unmöglichkeit, natives Pinch-Zoom zu deaktivieren, ist eine &quot;Funktion&quot;des HTC UI Wrapper (HTC Sense). Diese Funktion kann dazu führen, dass eine ganze Seite zoomt, wenn im Viewer die Geste &quot;Pinch to Zoom&quot;verwendet wird. Verwenden Sie stattdessen eine Doppeltippen-Geste.
* Imagemap-Symbole überlappen sich, wenn Imagemaps klein sind und nahe beieinander liegen.

## HTML5-Video-Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` -Modifikator wird nur bei Software-HLS- und Flash-HDS-Wiedergabe unterstützt. Es funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
* Die progressive OGG- und WebM-Wiedergabe wird nicht unterstützt.
* Die Browserskalierung bewirkt, dass der Videoplayer eine falsche Größe anzeigt (einschließlich Anzeigeeinstellungen für Windows® Control Panel ).
* Die Verwendung von HLS-Streaming in Safari bei der Videosuche ist inkonsistent.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Der Quirks-Modus wird nicht unterstützt.
* Der Kompatibilitätsmodus wird nicht unterstützt.
* Internet Explorer auf Mobilgeräten wird nicht unterstützt.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Große eKataloge führen auf dem iPad 2 zum Absturz des Browsers.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 oder höher: Die Einstellungen des Internet-Plug-ins verhindern die Wiedergabe von Flash-Videos.
* Die Verwendung von HLS-Streaming in Safari bei der Videosuche ist inkonsistent.
* Das Ende des Videos in Safari 6 kann nicht mithilfe von HLS-Streaming gesucht werden.
