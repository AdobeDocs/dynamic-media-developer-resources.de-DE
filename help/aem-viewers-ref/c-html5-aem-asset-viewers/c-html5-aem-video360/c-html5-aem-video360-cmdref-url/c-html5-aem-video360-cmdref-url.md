---
description: Dokumentation zur Befehlsreferenz für Video360 Viewer.
solution: Experience Manager
title: Befehlsreferenz - URL
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Befehlsreferenz - URL{#command-reference-url}

Dokumentation zur Befehlsreferenz für Video360 Viewer.

Sie können einen beliebigen Konfigurationsbefehl in der URL festlegen. Sie können auch die API-Methoden `setParam()`, `setParams()` oder beides verwenden, um einen beliebigen Konfigurationsbefehl festzulegen. Sie können auch jedes Konfigurationsattribut im serverseitigen Konfigurationseintrag angeben.

Sie können einigen Konfigurationsbefehlen das Präfix mit dem Klassennamen oder dem Instanznamen der entsprechenden HTML5 Viewer SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält optionale Präfixe für solche Befehle. `playback` wird beispielsweise wie folgt dokumentiert:

```
[Video360Player.|<containerId>_video360Player].playback
```

bedeutet, dass dieser Befehl wie folgt verwendet wird:

* `playback` (kurze Syntax)
* `Video360Player.playback` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_video360Player.playback` (qualifiziert mit Komponenten-ID, vorausgesetzt, dass  `cont` die ID des Container-Elements ist)

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
