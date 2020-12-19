---
description: Dokumentation zur Befehlsreferenz für Video360 Viewer.
seo-description: Dokumentation zur Befehlsreferenz für Video360 Viewer.
seo-title: Befehlsreferenz - URL
solution: Experience Manager
title: Befehlsreferenz - URL
topic: Dynamic media
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Befehlsreferenz - URL{#command-reference-url}

Dokumentation zur Befehlsreferenz für Video360 Viewer.

Sie können jeden Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()` oder `setParams()` oder beide verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Sie können bestimmten Konfigurationsbefehlen den Klassennamen oder den Instanznamen der entsprechenden HTML5 Viewer-SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält optionale Präfixe für solche Befehle. Zum Beispiel wird `playback` wie folgt dokumentiert:

```
[Video360Player.|<containerId>_video360Player].playback
```

Dies bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `playback` (kurze Syntax)
* `Video360Player.playback` (qualifiziert mit Komponentenklassenname)
* `cont_video360Player.playback` (mit Komponenten-ID qualifiziert, vorausgesetzt, dass dies die ID des Container-Elements  `cont` ist)

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz, die allen Viewern gemein ist - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
