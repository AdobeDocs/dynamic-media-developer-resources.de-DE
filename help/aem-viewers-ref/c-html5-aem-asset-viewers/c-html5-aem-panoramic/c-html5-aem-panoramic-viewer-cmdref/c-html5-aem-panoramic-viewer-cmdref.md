---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für den Panorama-Viewer.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

Dokumentation zu Konfigurationsattributen für den Panorama-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mithilfe von `setParam()`- und/oder `setParams()`-API-Methoden festgelegt werden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationsdatensatz angegeben werden.

Einigen Konfigurationsbefehlen kann der Klassenname oder der Instanzname der entsprechenden HTML5 SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispielsweise wird `vrrender` Befehl wie folgt dokumentiert:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `vrrender` (kurze Syntax)
* `PanoramicView.vrrender` (qualifiziert mit dem Komponentennamen)
* `cont_panoramicView.vrrender` (qualifiziert mit Komponenten-ID, unter der Annahme, dass count die ID des Container-Elements ist)


Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Siehe [Befehlsreferenz, die für alle Viewer verwendet wird - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
