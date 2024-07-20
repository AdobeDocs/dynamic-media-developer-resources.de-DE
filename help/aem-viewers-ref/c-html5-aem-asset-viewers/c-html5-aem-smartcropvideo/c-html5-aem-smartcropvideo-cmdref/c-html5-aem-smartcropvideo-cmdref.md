---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
source-git-commit: eaf59166fcc1ff8ec5a2e846ef0eb180c8cbdd5a
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Smart Crop Video Viewer.

Sie können einen beliebigen Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()`, `setParams()` oder beide verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationseintrag angeben.

Sie können einigen Konfigurationsbefehlen das Präfix mit dem Klassennamen oder dem Instanznamen der entsprechenden Viewer SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des an die API-Methode `setContainerId()` übergebenen Viewer-Container-DOM-Elements ab. Die Dokumentation enthält optionale Präfixe für solche Befehle. Beispiel: `playback` wird wie folgt dokumentiert:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Das bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `playback` (kurze Syntax)
* `SmartCropVideoPlayer.playback` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_videoPlayer.playback` (qualifiziert mit Komponenten-ID, vorausgesetzt, `cont` ist die ID des Container-Elements)

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Siehe [Befehlsreferenz für alle Viewer - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
