---
title: Befehlsreferenz - URL
description: Dokumentation zur Befehlsreferenz für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Befehlsreferenz - URL{#command-reference-url}

Dokumentation zur Befehlsreferenz für Video-Viewer.

Sie können einen beliebigen Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()`, `setParams()` oder beide verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationseintrag angeben.

Sie können einigen Konfigurationsbefehlen das Präfix mit dem Klassennamen oder dem Instanznamen der entsprechenden Viewer SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des an die API-Methode `setContainerId()` übergebenen Viewer-Container-DOM-Elements ab. Die Dokumentation enthält optionale Präfixe für solche Befehle. Beispiel: `playback` wird wie folgt dokumentiert:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_videoPlayer.playback` (qualifiziert mit Komponenten-ID, vorausgesetzt, `cont` ist die ID des Container-Elements)

Siehe auch [für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Siehe auch [Befehlsreferenz für alle Viewer - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
