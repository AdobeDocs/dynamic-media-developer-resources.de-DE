---
title: Bild vorausfüllen
description: Bild vorladen ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und angezeigt wird, während Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen heruntergeladen werden. Der Zweck des vorausgefüllten Bildes ist es, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell zu präsentieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Bild vorausfüllen{#preload-image}

Bild vorladen ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und angezeigt wird, während Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen heruntergeladen werden. Der Zweck des vorausgefüllten Bildes ist es, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell zu präsentieren.

Das Vorausfüllen des Bildes funktioniert gut für die gängigste Methode zum Einbetten von Viewern, die responsive Einbettung mit unbegrenzter Höhe ist. Siehe die Überschrift [Responsives Design Einbetten mit unbegrenzter Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Die Funktion weist jedoch bestimmte Einschränkungen auf, wenn andere Einbettungsmethoden oder bestimmte Konfigurationsoptionen verwendet werden. Das Vorabladen des Bildes kann in folgenden Fällen möglicherweise nicht ordnungsgemäß gerendert werden:

* Wenn die Größe des Viewers festgelegt ist und die Größe entweder mithilfe `stagesize` Konfigurationsattributs im Viewer-Vorgabendatensatz oder in der CSS-Datei des externen Viewers für das Viewer-Container-Element der obersten Ebene definiert wird.
* Bei Verwendung der flexiblen Einbettungsmethode mit Breite und Höhe definierte Methode der Viewer-Einbettung. Siehe die Überschrift [Flexible Einbettung mit definierter Breite und Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Wenn Sie den Viewer in einem der oben aufgeführten Betriebsmodi verwenden, deaktivieren Sie die Funktion „Bild vorab laden“ mit dem Konfigurationsattribut &quot;`preloadImage`&quot;.

Außerdem wird das Vorabladen von Bildern nicht verwendet, auch wenn es in der Konfiguration aktiviert ist, wenn der Viewer in das DOM-Element eingebettet ist, mit `display:none` CSS-Einstellung ausgeblendet oder von der DOM-Struktur getrennt wird.
