---
title: Befehlsreferenz - Konfigurationsattribute
description: Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
TQID: 'https://experienceleague.adobe.com/NRcFJ2RyskUxLayfdSmJ-jk-rHjPWiOWt0XwQJ7tvM8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# Befehlsreferenz - Konfigurationsattribute{#command-reference-configuration-attributes}

Dokumentation zu Konfigurationsattributen für den E-Katalog-Viewer.

Jeder Konfigurationsbefehl kann in der URL oder mithilfe von `setParam()`, `setParams()` oder beiden API-Methoden festgelegt werden. Sie können auch jedes Konfigurationsattribut angeben, das im serverseitigen Konfigurationsdatensatz angegeben ist.

Bei einigen Konfigurationsbefehlen können Sie ihnen den Klassennamen oder Instanznamen der entsprechenden Viewer-SDK-Komponente voranstellen. Ein Instanzname der Komponente ist dynamisch und hängt von der ID des Viewer-Container-DOM-Elements ab, das an `setContainerId()` API-Methode übergeben wird. Die Dokumentation enthält ein optionales Präfix für solche Befehle. Beispielsweise wird `zoomstep` Befehl wie folgt dokumentiert:

`[PageView.|<containerId>_pageView].zoomstep`

Das bedeutet, dass Sie diesen Befehl wie folgt verwenden können

* `zoomstep` (kurze Syntax)
* `PageView.zoomstep` (qualifiziert mit dem Komponentennamen)
* `cont_pageView.zoomstep` (qualifiziert mit Komponenten-ID, vorausgesetzt, `cont` ist die ID des Container-Elements)

Siehe auch [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
