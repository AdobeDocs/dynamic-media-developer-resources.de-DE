---
description: Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.
seo-description: Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.
seo-title: Befehlsreferenz - Konfigurationsattribute
solution: Experience Manager
title: Befehlsreferenz - Konfigurationsattribute
topic: Dynamic Media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mit den API-Methoden `setParam()`, `setParams()` oder  oder beide festgelegt werden. Sie können auch jedes Konfigurationsattribut angeben, das im serverseitigen Konfigurationssatz angegeben ist.

Bei einigen Konfigurationsbefehlen können Sie ihnen den Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an die API-Methode `setContainerId()` übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomstep` wird beispielsweise wie folgt dokumentiert:

`[PageView.|<containerId>_pageView].zoomstep`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können:

* `zoomstep` (kurze Syntax)
* `PageView.zoomstep` (qualifiziert mit Komponentenklassenname)
* `cont_pageView.zoomstep` (mit Komponenten-ID qualifiziert, vorausgesetzt,  `cont` die ID des Container-Elements ist vorhanden)

Siehe auch [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
