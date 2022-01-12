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

Sie können jeden Konfigurationsbefehl in URL festlegen. Oder Sie können `setParam()`, `setParams()`oder beide API-Methoden. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationssatz angeben.

Einige Konfigurationsbefehle erhalten das Präfix Klassenname oder Instanzname der entsprechenden Viewer-SDK-Komponente. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an übergeben wird `setContainerId()` API-Methode. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispiel: die `zoomfactor` -Befehl wird wie folgt dokumentiert:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Der Befehl wird wie folgt verwendet:

* `zoomfactor` (kurze Syntax)
* `FlyoutZoomView.zoomfactor` (qualifiziert mit einem Komponentenklassennamen)
* `cont_flyout.zoomfactor` (qualifiziert mit der Komponenten-ID, vorausgesetzt, dass `cont` ist die ID des Containerelements)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
