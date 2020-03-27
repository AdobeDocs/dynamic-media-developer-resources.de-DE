---
description: Dokumentation zu Konfigurationsattributen für Karussell-Viewer.
seo-description: Dokumentation zu Konfigurationsattributen für Karussell-Viewer.
seo-title: Befehlsreferenz - Konfigurationsattribute
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
topic: Dynamic media
uuid: 036af728-ab00-4db3-98cf-d16f1bffa064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Karussell-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mit `setParam()`oder `setParams()`oder beidem API-Methoden festgelegt werden. Jedes config-Attribut kann auch im serverseitigen Konfigurationssatz angegeben werden.

Einige Konfigurationsbefehle können mit dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente versehen werden. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der `zoomstep` Befehl wird beispielsweise wie folgt dokumentiert:

`[ZoomView.|<containerId>_carouselView].fmt`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `fmt` (kurze Syntax)
* `CarouselView.fmt` (qualifiziert mit Komponentenklassenname)
* `cont_carouselView.fmt` (mit Komponenten-ID qualifiziert, vorausgesetzt, `cont` die ID des Container-Elements ist vorhanden)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
