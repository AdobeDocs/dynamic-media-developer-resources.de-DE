---
description: Dokumentation zu Konfigurationsattributen für Video360 Viewer.
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für Video360 Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mit den API-Methoden `setParam()`, `setParams()` oder  oder beide festgelegt werden. Jedes Konfigurationsattribut kann auch im serverseitigen Konfigurationssatz angegeben werden.

Einige Konfigurationsbefehle können mit dem Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente versehen werden. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `playback` wird beispielsweise wie folgt dokumentiert:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `playback` (kurze Syntax)
* `VideoPlayer.playback` (qualifiziert mit Komponentenklassenname)
* `cont_videoPlayer.playback` (mit Komponenten-ID qualifiziert, vorausgesetzt,  `cont` die ID des Container-Elements ist vorhanden)

Siehe auch [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
