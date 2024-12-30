---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Video Viewer.

Sie können einen beliebigen Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()`, `setParams()` oder beides verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch ein beliebiges Konfigurationsattribut im serverseitigen Konfigurationsdatensatz angeben.

Einigen Konfigurationsbefehlen können der Klassenname oder der Instanzname der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält optionale Präfixe für solche Befehle. `playback` wird beispielsweise wie folgt dokumentiert:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit dem Komponentennamen)
* `cont_videoPlayer.playback` (qualifiziert mit Komponenten-ID, unter der Annahme, dass `cont` die ID des Container-Elements ist)

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Siehe [Befehlsreferenz, die für alle Viewer verwendet wird - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
