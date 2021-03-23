---
description: Dokumentation zu Konfigurationsattributen für den Flyout-Viewer
seo-description: Dokumentation zu Konfigurationsattributen für den Flyout-Viewer
seo-title: Befehlsreferenz - Konfigurationsattribute
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
uuid: d7e89a24-a235-4f20-86d1-25aacd118880
feature: Dynamic Media Classic, Viewer, SDK/API, Flyout
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den Flyout-Viewer

Sie können jeden Konfigurationsbefehl in der URL festlegen. Oder Sie können `setParam()`, `setParams()` oder beide API-Methoden verwenden. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Einige Konfigurationsbefehle erhalten den Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomfactor` wird beispielsweise wie folgt dokumentiert:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Der Befehl wird wie folgt verwendet:

* `zoomfactor` (kurze Syntax)
* `FlyoutZoomView.zoomfactor` (qualifiziert mit einem Komponentenklassennamen)
* `cont_flyout.zoomfactor` (mit der Komponenten-ID qualifiziert, vorausgesetzt, dass dies die ID des Container-Elements  `cont` ist)

Siehe auch [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
