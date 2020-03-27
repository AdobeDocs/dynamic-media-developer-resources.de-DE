---
description: Dokumentation zur Befehlsreferenz für Video Viewer.
seo-description: Dokumentation zur Befehlsreferenz für Video Viewer.
seo-title: Befehlsreferenz - URL
solution: Experience Manager
title: Befehlsreferenz - URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4

---


# Befehlsreferenz - URL{#command-reference-url}

Dokumentation zur Befehlsreferenz für Video Viewer.

Sie können jeden Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()`oder `setParams()`oder beide verwenden, um einen Konfigurationsbefehl festzulegen. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Sie können bestimmten Konfigurationsbefehlen den Klassennamen oder den Instanznamen der entsprechenden Viewer-SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält optionale Präfixe für solche Befehle. Zum Beispiel `playback` wird wie folgt dokumentiert:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Dies bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit Komponentenklassenname)
* `cont_videoPlayer.playback` (mit Komponenten-ID qualifiziert, vorausgesetzt, dass dies die ID des Container-Elements `cont` ist)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Siehe auch [Befehlsreferenz für alle Viewer - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
