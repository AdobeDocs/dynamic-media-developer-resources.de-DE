---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für Flyout-Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Flyout-Viewer

Sie können jeden Konfigurationsbefehl in URL festlegen. Oder Sie können `setParam()`, `setParams()` oder beide API-Methoden verwenden. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Einige Konfigurationsbefehle erhalten das Präfix Klassenname oder Instanzname der entsprechenden Viewer-SDK-Komponente. Der Instanzname der Komponente ist dynamisch und hängt von der ID des an die API-Methode `setContainerId()` übergebenen Viewer-Container-DOM-Elements ab. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomfactor` wird beispielsweise wie folgt dokumentiert:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Der Befehl wird wie folgt verwendet:

* `zoomfactor` (kurze Syntax)
* `FlyoutZoomView.zoomfactor` (qualifiziert mit dem Namen einer Komponentenklasse)
* `cont_flyout.zoomfactor` (qualifiziert mit der Komponenten-ID, vorausgesetzt, `cont` ist die ID des Container-Elements)

Siehe auch [für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
