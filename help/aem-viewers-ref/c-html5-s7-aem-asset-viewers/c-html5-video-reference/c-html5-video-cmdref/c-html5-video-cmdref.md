---
description: Dokumentation zu Konfigurationsattributen für Video Viewer.
seo-description: Dokumentation zu Konfigurationsattributen für Video Viewer.
seo-title: Befehlsreferenz - Konfigurationsattribute
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Video Viewer.

Sie können jeden Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()` oder `setParams()` oder beide verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Sie können bestimmten Konfigurationsbefehlen den Klassennamen oder den Instanznamen der entsprechenden Viewer-SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält optionale Präfixe für solche Befehle. Zum Beispiel wird `playback` wie folgt dokumentiert:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Dies bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit Komponentenklassenname)
* `cont_videoPlayer.playback` (mit Komponenten-ID qualifiziert, vorausgesetzt, dass dies die ID des Container-Elements  `cont` ist)

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Siehe [Befehlsreferenz, die allen Viewern gemein ist - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
