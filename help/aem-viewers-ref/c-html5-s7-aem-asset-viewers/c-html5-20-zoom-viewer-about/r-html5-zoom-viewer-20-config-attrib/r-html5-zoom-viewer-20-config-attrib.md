---
description: Dokumentation zu Konfigurationsattributen für den Zoom-Viewer.
seo-description: Dokumentation zu Konfigurationsattributen für den Zoom-Viewer.
seo-title: Befehlsreferenz - Konfigurationsattribute
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
uuid: 1bcc879a-12ec-4924-ac05-2e4c1d6e4597
feature: Dynamic Media Classic, Viewer, SDK/API, Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den Zoom-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mit den API-Methoden `setParam()`, `setParams()` oder  oder beide festgelegt werden. Jedes config-Attribut kann auch im serverseitigen Konfigurationssatz angegeben werden.

Einige Konfigurationsbefehle können mit dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente versehen werden. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomstep` wird beispielsweise wie folgt dokumentiert:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `zoomstep` (kurze Syntax)
* `ZoomView.zoomstep` (qualifiziert mit Komponentenklassenname)
* `cont_zoomView.zoomstep` (mit Komponenten-ID qualifiziert, vorausgesetzt,  `cont` die ID des Container-Elements ist vorhanden)

Siehe auch [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
