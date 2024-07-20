---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.

Jeder Konfigurationsbefehl kann in URL oder mit `setParam()`, `setParams()` oder beiden API-Methoden festgelegt werden. Sie können auch jedes Konfigurationsattribut angeben, das im serverseitigen Konfigurationssatz angegeben ist.

Bei einigen Konfigurationsbefehlen können Sie ihnen den Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente voranstellen. Der Instanzname der Komponente ist dynamisch und hängt von der ID des an die API-Methode `setContainerId()` übergebenen Viewer-Container-DOM-Elements ab. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Der Befehl `zoomstep` wird beispielsweise wie folgt dokumentiert:

`[PageView.|<containerId>_pageView].zoomstep`

Das bedeutet, dass Sie diesen Befehl als

* `zoomstep` (kurze Syntax)
* `PageView.zoomstep` (qualifiziert mit dem Namen der Komponentenklasse)
* `cont_pageView.zoomstep` (qualifiziert mit Komponenten-ID, vorausgesetzt `cont` ist die ID des Container-Elements)

Siehe auch [für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
