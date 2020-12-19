---
description: Das Vorlade-Bild ist ein Bild für die Vorschau von statischen Assets, das direkt nach dem Aufruf der init()-Methode geladen wird und das beim Herunterladen von Viewer-SDK-Bibliotheken sowie von Asset- und Vorgabeninformationen angezeigt wird. Das Vorlade-Bild dient dazu, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell bereitzustellen.
seo-description: Das Vorlade-Bild ist ein Bild für die Vorschau von statischen Assets, das direkt nach dem Aufruf der init()-Methode geladen wird und das beim Herunterladen von Viewer-SDK-Bibliotheken sowie von Asset- und Vorgabeninformationen angezeigt wird. Das Vorlade-Bild dient dazu, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell bereitzustellen.
seo-title: Vorab-Bild
solution: Experience Manager
title: Vorab-Bild
topic: Dynamic media
uuid: bae99269-fd55-485e-b78e-873b77541d91
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Bild vor dem Laden{#preload-image}

Das Vorlade-Bild ist ein Bild für die Vorschau von statischen Assets, das direkt nach dem Aufruf der init()-Methode geladen wird und das beim Herunterladen von Viewer-SDK-Bibliotheken sowie von Asset- und Vorgabeninformationen angezeigt wird. Das Vorlade-Bild dient dazu, die Ladezeit des Viewers visuell zu verbessern und dem Benutzer Inhalte schnell bereitzustellen.

Das Vorlade-Bild funktioniert bei der gängigsten Viewer-Einbettungsmethode, bei der reaktionsfähiges Einbetten mit uneingeschränkter Höhe erfolgt. Siehe die Überschrift [Einbettung von Responsive Design mit unbeschränkter Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Die Funktion hat jedoch gewisse Einschränkungen, wenn andere Einbettungsmethoden oder bestimmte Konfigurationsoptionen verwendet werden. In folgenden Fällen kann das Vorladen des Bildes fehlschlagen:

* Wenn die Größe des Viewers festgelegt ist und die Größe entweder mit dem Konfigurationsattribut `stagesize` im Viewer-Vorgabendatensatz oder in der externen Viewer-CSS-Datei für das Element des Viewer-Containers der obersten Ebene definiert wird.
* Wenn die Einbettung in flexibler Größe mit der definierten Breite- und Höhe des Viewers verwendet wird. Siehe Überschrift [Einbettung flexibler Größe mit definierter Breite und Höhe](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Wenn Sie den Viewer in einem der oben aufgeführten Betriebsmodi verwenden, müssen Sie die Funktion für das Vorladen von Bildern möglicherweise mit dem Konfigurationsattribut `preloadImage` deaktivieren.

Außerdem wird das Vorlade-Bild nicht verwendet - auch wenn es in der Konfiguration aktiviert ist - wenn der Viewer in das DOM-Element eingebettet ist und die CSS-Einstellung `display:none` verwendet oder von der DOM-Struktur getrennt wird.
