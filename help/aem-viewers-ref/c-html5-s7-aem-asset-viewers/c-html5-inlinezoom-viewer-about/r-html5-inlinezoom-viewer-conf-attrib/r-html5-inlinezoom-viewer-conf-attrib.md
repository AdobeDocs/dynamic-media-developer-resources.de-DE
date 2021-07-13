---
description: Dokumentation zu Konfigurationsattributen für Flyout-Viewer
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,Viewer,SDK/API,Inline-Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Flyout-Viewer

Sie können jeden Konfigurationsbefehl in URL festlegen. Oder Sie können `setParam()`, `setParams()` oder beide API-Methoden verwenden. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Einige Konfigurationsbefehle erhalten das Präfix Klassenname oder Instanzname der entsprechenden Viewer-SDK-Komponente. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomfactor` wird beispielsweise wie folgt dokumentiert:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Der Befehl wird wie folgt verwendet:

* `zoomfactor` (kurze Syntax)
* `FlyoutZoomView.zoomfactor` (qualifiziert mit einem Komponentenklassennamen)
* `cont_flyout.zoomfactor` (qualifiziert mit der Komponenten-ID, vorausgesetzt, dass  `cont` die ID des Container-Elements ist)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
