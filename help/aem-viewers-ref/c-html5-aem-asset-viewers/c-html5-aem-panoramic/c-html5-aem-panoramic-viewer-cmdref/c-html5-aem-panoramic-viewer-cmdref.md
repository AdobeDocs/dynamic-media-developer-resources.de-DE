---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für Panorama-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Panorama-Viewer.

Jeder Konfigurationsbefehl kann in URL oder mithilfe von `setParam()` und/oder `setParams()` API-Methoden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationseintrag angegeben werden.

Einige Konfigurationsbefehle können dem Klassennamen oder Instanznamen der entsprechenden HTML5 SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an übergeben wird `setContainerId()` API-Methode. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispiel: `vrrender` -Befehl wird wie folgt dokumentiert:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `vrrender` (kurze Syntax)
* `PanoramicView.vrrender` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_panoramicView.vrrender` (mit Komponenten-ID qualifiziert, vorausgesetzt, der Inhalt ist die ID des Container-Elements)


Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Siehe [Befehlsreferenz für alle Viewer - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
