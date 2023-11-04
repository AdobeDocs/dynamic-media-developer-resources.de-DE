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

Jeder Konfigurationsbefehl kann in URL oder mithilfe von `setParam()`oder `setParams()`oder beides API-Methoden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationseintrag angegeben werden.

Einige Konfigurationsbefehle können dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an übergeben wird `setContainerId()` API-Methode. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispiel: `zoomstep` -Befehl wird wie folgt dokumentiert:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Das bedeutet, dass Sie den Befehl als

* `zoomstep` (kurze Syntax)
* `ZoomView.zoomstep` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_zoomView.zoomstep` (qualifiziert mit Komponenten-ID, vorausgesetzt `cont` ist die ID des Containerelements)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
