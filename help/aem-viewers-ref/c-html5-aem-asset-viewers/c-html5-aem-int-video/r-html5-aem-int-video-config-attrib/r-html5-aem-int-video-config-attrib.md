---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 80b7971c-82dc-47a2-adde-9e061a0f856d
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den interaktiven Video-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mithilfe von `setParam()`, `setParams()` oder beiden API-Methoden festgelegt werden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationsdatensatz angegeben werden.

Einigen Konfigurationsbefehlen kann der Klassenname oder Instanzname der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispielsweise wird `playback` Befehl wie folgt dokumentiert:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Und bedeutet, dass Sie den folgenden Befehl verwenden können:

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit dem Komponentennamen)
* `cont_videoPlayer.playback` (qualifiziert mit Komponenten-ID, vorausgesetzt, `cont` ist die ID des Container-Elements)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
