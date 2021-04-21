---
description: Dokumentation zu Konfigurationsattributen für den Flyout-Viewer
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
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
