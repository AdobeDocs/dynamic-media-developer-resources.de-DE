---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für den Panorama-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den Panorama-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mithilfe von `setParam()`- und/oder `setParams()`-API-Methoden festgelegt werden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationsdatensatz angegeben werden.

Einigen Konfigurationsbefehlen kann der Klassenname oder der Instanzname der entsprechenden HTML5-SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispielsweise wird `vrrender` Befehl wie folgt dokumentiert:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `vrrender` (kurze Syntax)
* `PanoramicView.vrrender` (qualifiziert mit dem Komponentennamen)
* `cont_panoramicView.vrrender` (qualifiziert mit Komponenten-ID, unter der Annahme, dass count die ID des Container-Elements ist)


Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Siehe [Befehlsreferenz, die für alle Viewer verwendet wird - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
