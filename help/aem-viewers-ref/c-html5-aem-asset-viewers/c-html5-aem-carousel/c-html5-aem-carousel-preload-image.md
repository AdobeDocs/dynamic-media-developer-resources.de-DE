---
title: Vorab-Bild
description: Das Vorlade-Bild ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und beim Herunterladen von Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen angezeigt wird. Das Vorlade-Bild soll die Ladezeit des Viewers visuell verbessern und dem Benutzer Inhalte schnell präsentieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Vorab-Bild{#preload-image}

Das Vorlade-Bild ist ein statisches Asset-Vorschaubild, das direkt nach dem Aufruf der init()-Methode geladen wird und beim Herunterladen von Viewer-SDK-Bibliotheken, -Assets und -Vorgabeninformationen angezeigt wird. Das Vorlade-Bild soll die Ladezeit des Viewers visuell verbessern und dem Benutzer Inhalte schnell präsentieren.

Das Vorabladen von Bildern eignet sich gut für die gängigste Viewer-Einbettungsmethode, bei der eine responsive Einbettung mit uneingeschränkter Höhe erfolgt. Siehe Überschrift [Responsives Design, das mit unbeschränkter Höhe eingebettet wird](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Die Funktion weist jedoch bestimmte Einschränkungen auf, wenn andere Einbettungsmethoden oder bestimmte Konfigurationsoptionen verwendet werden. In folgenden Fällen kann das Vorausfüllen des Bildes nicht ordnungsgemäß dargestellt werden:

* Wenn der Viewer eine feste Größe hat und die Größe entweder mithilfe des Konfigurationsattributs `stagesize` innerhalb des Viewer-Vorgabendatensatzes oder in der externen Viewer-CSS-Datei für das Viewer-Container-Element der obersten Ebene definiert wird.
* Bei Verwendung der flexiblen Größe, die mit der Breite und Höhe definierten Methode der Viewer-Einbettung einbettet wird. Siehe Überschrift [Flexible Größe, eingebettet in Breite und Höhe definiert](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Wenn Sie den Viewer in einem der oben aufgeführten Vorgangsmodi verwenden, deaktivieren Sie die Funktion zum Vorausfüllen des Bildes mithilfe des Konfigurationsattributs `preloadImage` .

Außerdem wird das Vorlade-Bild nicht verwendet - auch wenn es in der Konfiguration aktiviert ist - wenn der Viewer in das DOM-Element eingebettet ist und die CSS-Einstellung `display:none` verwendet oder von der DOM-Struktur getrennt ist.
