---
description: Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.

Jeder Konfigurationsbefehl kann in URL oder mit `setParam()`, `setParams()` oder beiden API-Methoden festgelegt werden. Sie können auch jedes Konfigurationsattribut angeben, das im serverseitigen Konfigurationssatz angegeben ist.

Bei einigen Konfigurationsbefehlen können Sie ihnen den Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des an die API-Methode `setContainerId()` übergebenen Viewer-Container-DOM-Elements ab. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomstep` wird beispielsweise wie folgt dokumentiert:

`[PageView.|<containerId>_pageView].zoomstep`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `zoomstep` (kurze Syntax)
* `PageView.zoomstep` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_pageView.zoomstep` (qualifiziert mit Komponenten-ID, vorausgesetzt `cont` ist die ID des Container-Elements)

Siehe auch [für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
