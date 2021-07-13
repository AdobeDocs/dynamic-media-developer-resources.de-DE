---
description: Dokumentation zu Konfigurationsattributen für den Rotationsset-Viewer.
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,Viewer,SDK/API,Rotationssets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den Rotationsset-Viewer.

Jeder Konfigurationsbefehl kann in URL oder mit `setParam()`, `setParams()` oder beidem API-Methoden festgelegt werden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationseintrag angegeben werden.

Einige Konfigurationsbefehle können dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomstep` wird beispielsweise wie folgt dokumentiert:

`[SpinView.|<containerId>_spinView].zoomstep`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `zoomstep` (kurze Syntax)
* `SpinView.zoomstep` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_spinView.zoomstep` (qualifiziert mit Komponenten-ID, vorausgesetzt,  `cont` die ID des Container-Elements ist)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
