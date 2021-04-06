---
description: Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.
solution: Experience Manager
title: Anmerkungen zur Kompatibilität
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Kompatibilitätsanweisungen{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Kompatibilitätshinweise für Betriebssysteme, Browser und Mobilgeräte.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Inkompatibilität mit älteren adaptiven Video-Sets. Adaptive Video-Sets erneut laden, um die Wiedergabe zu ermöglichen.

## Allgemein {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Die seitliche Skalierung des Browsers bewirkt, dass die Benutzeroberfläche und die Bilder verschwommen werden, wenn der Benutzer die Seite vergrößert. Die Formatierung der Benutzeroberfläche wird je nach Zoom ebenfalls falsch angezeigt und wird in den Vollbildmodus übertragen.
* Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien eine Foliengeste, um Frames in eingebetteten Bildsätzen auszutauschen, anstatt auf die Komponente für eingebettete Muster zu tippen. Komponente ist als visueller Indikator vorhanden.
* In Internet Explorer-Browsern und einigen Touch-Geräten nimmt der Vollbildmodus nicht den gesamten Gerätebildschirm ein. Stattdessen wird die Größe der Anwendung an die Größe des Browserfensters angepasst.
* Die Schaltfläche &quot;Schließen&quot;funktioniert unter iOS 8.0 und iOS 8.1 nicht, funktioniert aber unter iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Speicherleck bei Zoom- und E-Katalog-Viewern. Die wiederholte Navigation durch Frames führt zum Absturz des Browsers.
* Durch Tippen auf die Dublette in einem Viewer wird die gesamte Seite gezoomt und nicht nur der Viewer mit aktivierter browserseitiger Skalierung.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Gerät, das im Hochformat als Tablet erkannt wird und bei Vollbild in den Browsereinstellungen aktiviert ist.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Durch Tippen auf die Dublette in einem Viewer wird die gesamte Seite statt nur des Viewers gezoomt, wobei die Browser-seitige Skalierung aktiviert ist.

## Galaxy Nexus 10 und Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* Der E-Katalog zeigt einen falschen Seitenbogen mit Ausrichtung im Hoch- und Querformat an.

## HTC Mobile Devices {#section-dc42c80414c842e488738fc157c55b01}

* Die Unmöglichkeit, natives Pinch-Zoom zu deaktivieren, ist eine &quot;Funktion&quot; des HTC UI Wrapper (HTC Sense). Diese Funktion kann dazu führen, dass die gesamte Seite mit der Geste &quot;Zum Zoomen auf Pinch-to-Zoom&quot;im Viewer gezoomt wird. Verwenden Sie stattdessen eine Dublette-Tippen-Geste.
* Imagemap-Symbole überlappen, wenn Imagemaps klein und nahe beieinander sind.

## HTML5-Video-Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` -Modifikator wird nur für die Wiedergabe von Software-HLS und Flash-HDS unterstützt. Es funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
* Die progressive Wiedergabe von OGG und WebM wird nicht unterstützt.
* Die Browser-Skalierung führt dazu, dass der Videoplayer in einer falschen Größe angezeigt wird (einschließlich der Anzeigeeinstellungen der Windows®-Systemsteuerung).
* Die Suche nach Videos mit HLS-Streaming in Safari ist inkonsistent.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Der Quirks-Modus wird nicht unterstützt.
* Der Kompatibilitätsmodus wird nicht unterstützt.
* Internet Explorer auf Mobilgeräten wird nicht unterstützt.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Große E-Kataloge führen auf dem iPad 2 zum Absturz des Browsers.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 oder höher: Die Einstellungen des Internet-Plug-ins verhindern die Videowiedergabe im Flash.
* Die Suche nach Videos mit HLS-Streaming in Safari ist inkonsistent.
* Es kann nicht versucht werden, das Ende des Videos in Safari 6 mithilfe des HLS-Streaming zu suchen.
