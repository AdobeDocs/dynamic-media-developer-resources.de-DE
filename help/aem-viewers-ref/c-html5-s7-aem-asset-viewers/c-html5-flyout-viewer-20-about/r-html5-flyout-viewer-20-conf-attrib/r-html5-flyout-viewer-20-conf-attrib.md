---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für Flyout-Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Flyout-Viewer

Sie können einen beliebigen Konfigurationsbefehl in der URL festlegen. Sie können auch `setParam()`, `setParams()` oder beide API-Methoden verwenden. Sie können auch ein beliebiges Konfigurationsattribut im serverseitigen Konfigurationsdatensatz angeben.

Einigen Konfigurationsbefehlen wird der Klassenname oder Instanzname der entsprechenden Viewer-SDK-Komponente vorangestellt. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der `zoomfactor`-Befehl wird beispielsweise wie folgt dokumentiert:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Der Befehl wird wie folgt verwendet:

* `zoomfactor` (kurze Syntax)
* `FlyoutZoomView.zoomfactor` (qualifiziert mit dem Namen einer Komponentenklasse)
* `cont_flyout.zoomfactor` (qualifiziert mit der Komponenten-ID, unter der Annahme, dass `cont` die ID des Container-Elements ist)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
