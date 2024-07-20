---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für den Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den Zoom-Viewer.

Jeder Konfigurationsbefehl kann in URL oder mit `setParam()`, `setParams()` oder beiden API-Methoden festgelegt werden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationseintrag angegeben werden.

Einige Konfigurationsbefehle können dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Der Instanzname der Komponente ist dynamisch und hängt von der ID des an die API-Methode `setContainerId()` übergebenen Viewer-Container-DOM-Elements ab. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomstep` wird beispielsweise wie folgt dokumentiert:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Das bedeutet, dass Sie den Befehl als

* `zoomstep` (kurze Syntax)
* `ZoomView.zoomstep` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_zoomView.zoomstep` (qualifiziert mit Komponenten-ID, vorausgesetzt `cont` ist die ID des Container-Elements)

Siehe auch [für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
