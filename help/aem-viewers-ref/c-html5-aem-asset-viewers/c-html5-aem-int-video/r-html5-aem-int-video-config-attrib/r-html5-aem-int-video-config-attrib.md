---
description: Dokumentation zu Konfigurationsattributen für den interaktiven Video-Viewer.
seo-description: Dokumentation zu Konfigurationsattributen für den interaktiven Video-Viewer.
seo-title: Befehlsreferenz - Konfigurationsattribute
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
topic: Dynamic media
uuid: eaf7a1a2-b0ec-4df2-926b-5e2c4cd0b3d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den interaktiven Video-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mit `setParam()`oder `setParams()`oder beidem API-Methoden festgelegt werden. Jedes config-Attribut kann auch im serverseitigen Konfigurationssatz angegeben werden.

Einige Konfigurationsbefehle können mit dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente versehen werden. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der `playback` Befehl wird beispielsweise wie folgt dokumentiert:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit Komponentenklassenname)
* `cont_videoPlayer.playback` (mit Komponenten-ID qualifiziert, vorausgesetzt, `cont` die ID des Container-Elements ist vorhanden)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
