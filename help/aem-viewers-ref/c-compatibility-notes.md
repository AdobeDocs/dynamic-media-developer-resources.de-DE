---
description: Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.
seo-description: Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.
seo-title: Anmerkungen zur Kompatibilität
solution: Experience Manager
title: Anmerkungen zur Kompatibilität
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Anmerkungen zur Kompatibilität{#compatibility-notes}

Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Inkompatibilität mit älteren adaptiven Video-Sets. Möglicherweise müssen Sie adaptive Video-Sets erneut hochladen, um die Wiedergabe zu ermöglichen.

## Allgemein {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Die seitliche Skalierung des Browsers kann dazu führen, dass die Benutzeroberfläche und die Bilder verschwommen werden, wenn der Benutzer die Seite vergrößert. Die Formatierung der Benutzeroberfläche wird ggf. je nach Zoom falsch angezeigt. Dies wird in den Vollbildmodus übertragen.
* Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien eine Foliengeste, um Frames in eingebetteten Bildsätzen auszutauschen, anstatt auf die Komponente für eingebettete Muster zu tippen. Komponente ist als visueller Indikator vorhanden.
* In Internet Explorer-Browsern und einigen Touch-Geräten nimmt der Vollbildmodus nicht den gesamten Gerätebildschirm ein. Stattdessen wird die Größe der Anwendung an die Größe des Browserfensters angepasst.
* Die Schaltfläche &quot;Schließen&quot;funktioniert unter iOS 8.0 und iOS 8.1 nicht, funktioniert aber unter iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Speicherleck bei Zoom- und E-Katalog-Viewern. Wiederholte Navigation durch Frames kann zu einem Absturz des Browsers führen.
* Durch Tippen auf die Dublette in einem Viewer wird möglicherweise die gesamte Seite gezoomt und nicht nur der Viewer mit aktivierter browserseitiger Skalierung.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Gerät, das im Hochformat als Tablet erkannt wird und bei Vollbild in den Browsereinstellungen aktiviert ist.

## Galaxie Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Durch Tippen auf die Dublette in einem Viewer wird möglicherweise die gesamte Seite statt nur des Viewers gezoomt, wobei die Browser-seitige Skalierung aktiviert ist.

## Galaxy Nexus 10 und Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* Der E-Katalog zeigt einen falschen Seitenbogen mit Ausrichtung im Hoch- und Querformat an.

## HTC-Mobilgeräte {#section-dc42c80414c842e488738fc157c55b01}

* Die Unmöglichkeit, natives Pinch-Zoom zu deaktivieren, ist eine &quot;Funktion&quot; des HTC UI Wrapper (HTC Sense). Diese Funktion kann dazu führen, dass die gesamte Seite mit der Geste &quot;Zum Zoomen auf Pinch-to-Zoom&quot;im Viewer gezoomt wird. Verwenden Sie stattdessen eine Dublette-Tippen-Geste.
* Imagemap-Symbole können sich überlappen, wenn Imagemaps klein und nahe beieinander sind.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` wird nur bei Software-HLS und Flash-HDS-Wiedergabe unterstützt. Es funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
* Die progressive Wiedergabe von OGG und WebM wird nicht unterstützt.
* Die Browser-Skalierung kann dazu führen, dass der Videoplayer in einer falschen Größe angezeigt wird (einschließlich der Anzeigeeinstellungen des Windows OS-Bedienfelds).
* Die Suche nach Videos mit HLS-Streaming in Safari kann inkonsistent sein.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Der Quirks-Modus wird nicht unterstützt.
* Der Kompatibilitätsmodus wird nicht unterstützt.
* Internet Explorer auf Mobilgeräten wird nicht unterstützt.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Große E-Kataloge können dazu führen, dass der Browser auf dem iPad 2 abstürzt.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 oder höher: Mit den Einstellungen für das Internet-Plug-in kann die Wiedergabe von Flash-Videos verhindert werden.
* Die Suche nach Videos mit HLS-Streaming in Safari kann inkonsistent sein.
* Es kann nicht versucht werden, das Ende des Videos in Safari 6 mithilfe des HLS-Streaming zu suchen.

