---
title: Hinweise zur Kompatibilität
description: Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Hinweise zur Kompatibilität{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Inkompatibilität mit älteren adaptiven Videosets. Laden Sie adaptive Videosets erneut hoch, um die Wiedergabe zu ermöglichen.

## Allgemein {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Browser-seitige Skalierung führt dazu, dass Benutzeroberfläche und Bilder unscharf werden, wenn Benutzende die Seite vergrößern. Die Formatierung der Benutzeroberfläche wird auch je nach Zoom falsch angezeigt und in den Vollbildmodus übernommen.
* Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien Foliengesten, um Frames in eingebetteten Bildsets auszutauschen, anstatt auf die Komponente für eingebettete Farbfelder zu tippen. Die Komponente ist als visueller Indikator vorhanden.
* In Internet Explorer-Browsern und einigen Touch-Geräten belegt der Vollbildmodus nicht den gesamten Gerätebildschirm. Stattdessen wird die Größe der Anwendung an die Größe des Browser-Fensters angepasst.
* Die Schaltfläche „Schließen“ funktioniert nicht unter iOS 8.0 und iOS 8.1, aber unter iOS 8.2.

## Galaxie SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Speicherleck bei Zoom- und E-Katalog-Viewern. Wiederholte Navigation durch Frames führt zum Absturz des Browsers.
* Durch Doppeltippen auf einen Viewer wird die gesamte Seite vergrößert, anstatt nur der Viewer mit aktivierter Browser-seitiger Skalierung.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Gerät als Tablet im Hochformat erkannt, Vollbild in den Browser-Einstellungen überprüft.

## Galaxie Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Durch Doppeltippen auf einen Viewer wird die gesamte Seite vergrößert, anstatt nur der Viewer, wobei die browserseitige Skalierung aktiviert ist.

## Galaxy Nexus 10 und Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* Der E-Katalog zeigt eine falsche Seitenverteilung mit Hoch- und Querformat an.

## HTC-Mobilgeräte {#section-dc42c80414c842e488738fc157c55b01}

* Die Unfähigkeit, den nativen Pinch-Zoom zu deaktivieren, ist eine „Funktion“ des HTC UI Wrappers (HTC Sense). Diese Funktion kann dazu führen, dass eine ganze Seite vergrößert wird, wenn die Geste „Zum Zoomen drücken“ im Viewer verwendet wird. Verwenden Sie stattdessen eine Doppeltipp-Geste.
* Imagemap-Symbole überschneiden sich, wenn Imagemaps klein sind und nahe beieinander liegen.

## HTML5-Video-Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` Modifikator wird nur mit Software HLS und Flash HDS Wiedergabe unterstützt. Dies funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
* Die progressive Wiedergabe von OGG und WebM wird nicht unterstützt.
* Durch die Browser-Skalierung wird der Video-Player in einer falschen Größe angezeigt (einschließlich Anzeigeeinstellungen in der Windows®-Systemsteuerung).
* Videosuchvorgänge mit HLS-Streaming in Safari sind inkonsistent.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Der Quirks-Modus wird nicht unterstützt.
* Der Kompatibilitätsmodus wird nicht unterstützt.
* Internet Explorer auf Mobilgeräten wird nicht unterstützt.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Große E-Kataloge führen dazu, dass der Browser unter iPad 2 abstürzt.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 oder höher: Die Internet-Plug-in-Einstellungen verhindern die Flash-Videowiedergabe.
* Videosuchvorgänge mit HLS-Streaming in Safari sind inkonsistent.
* Die Suche nach dem Ende des Videos in Safari 6 mit HLS-Streaming ist nicht möglich.
