---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Video360 Viewer.

Jeder Konfigurationsbefehl kann in URL oder mithilfe von `setParam()`oder `setParams()`oder beides API-Methoden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationssatz angegeben werden.

Einige Konfigurationsbefehle können dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente vorangestellt werden. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an übergeben wird `setContainerId()` API-Methode. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispiel: `playback` -Befehl wird wie folgt dokumentiert:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Das bedeutet, dass Sie diesen Befehl in folgenden Fällen verwenden können:

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_videoPlayer.playback` (qualifiziert mit Komponenten-ID, vorausgesetzt `cont` ist die ID des Containerelements)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
