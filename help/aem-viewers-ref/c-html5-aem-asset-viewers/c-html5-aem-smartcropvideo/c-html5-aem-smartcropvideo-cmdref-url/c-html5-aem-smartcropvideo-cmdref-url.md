---
title: Befehlsreferenz - URL
description: Referenzdokumentation zum Befehl für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Befehlsreferenz - URL{#command-reference-url}

Referenzdokumentation zum Befehl für den Smart Crop Video Viewer.

Sie können einen beliebigen Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()`, `setParams()` oder beides verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch ein beliebiges Konfigurationsattribut im serverseitigen Konfigurationsdatensatz angeben.

Einigen Konfigurationsbefehlen können der Klassenname oder der Instanzname der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält optionale Präfixe für solche Befehle. `playback` wird beispielsweise wie folgt dokumentiert:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `playback` (kurze Syntax)
* `SmartCropVideoPlayer.playback` (qualifiziert mit dem Komponentennamen)
* `cont_smartCropVideoPlayer.playback` (qualifiziert mit Komponenten-ID, unter der Annahme, dass `cont` die ID des Container-Elements ist)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Siehe auch [Befehlsreferenz für alle Viewer - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
