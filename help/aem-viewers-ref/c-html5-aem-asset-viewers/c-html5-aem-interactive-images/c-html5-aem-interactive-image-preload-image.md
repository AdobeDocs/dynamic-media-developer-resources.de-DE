---
title: Vorab-Bild
description: Das Vorlade-Bild ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und beim Herunterladen von Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen angezeigt wird. Das Vorlade-Bild soll die Ladezeit des Viewers visuell verbessern und dem Benutzer Inhalte schnell präsentieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Vorab-Bild{#preload-image}

Das Vorlade-Bild ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und beim Herunterladen von Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen angezeigt wird. Das Vorlade-Bild soll die Ladezeit des Viewers visuell verbessern und dem Benutzer Inhalte schnell präsentieren.

Das Vorabladen von Bildern eignet sich gut für die gängigste Viewer-Einbettungsmethode, bei der eine responsive Einbettung mit uneingeschränkter Höhe erfolgt. Siehe Überschrift [Responsives Design, das mit unbeschränkter Höhe eingebettet wird](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Die Funktion weist jedoch bestimmte Einschränkungen auf, wenn andere Einbettungsmethoden oder bestimmte Konfigurationsoptionen verwendet werden. In folgenden Fällen kann das Vorausfüllen des Bildes nicht ordnungsgemäß dargestellt werden:

* Wenn der Viewer eine feste Größe hat und die Größe entweder mithilfe des Konfigurationsattributs `stagesize` innerhalb des Viewer-Vorgabendatensatzes definiert wird. Oder verwenden Sie die externe Viewer-CSS-Datei für das Viewer-Container-Element der obersten Ebene.
* Bei Verwendung der flexiblen Größe, die mit der Breite und Höhe definierten Methode der Viewer-Einbettung einbettet wird. Siehe Überschrift [Flexible Größe, eingebettet in Breite und Höhe definiert](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Deaktivieren Sie die Funktion zum Vorausfüllen von Bildern mit dem Konfigurationsattribut `preloadImage` , wenn Sie den Viewer in einem der oben aufgeführten Vorgangsmodi verwenden.

Außerdem wird das Vorlade-Bild nicht verwendet - auch wenn es in der Konfiguration aktiviert ist - wenn der Viewer in das DOM-Element eingebettet ist und die CSS-Einstellung `display:none` verwendet oder von der DOM-Struktur getrennt ist.
