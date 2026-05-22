---
title: PanoramicViewer
description: Der -Konstruktor erstellt eine HTML5-Instanz des Panorama-Viewers.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 4%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
Der -Konstruktor erstellt eine HTML5-Instanz des Panorama-Viewers.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} optionalem JSON-Konfigurationsobjekt können Sie alle Viewer-Einstellungen an den Konstruktor übergeben und den Aufruf einzelner Setter-Methoden vermeiden. Sie enthält die folgenden Eigenschaften:

* containerId - {String} ID des DOM-Containers (normalerweise ein DIV), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Container-Element zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn init() ausgeführt wird. Erforderlich
* params : {Object} JSON-Objekt mit Viewer-Konfigurationsparametern, wobei der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder ein SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender Einstellungswert ist. Erforderlich
* Handler : {Object} JSON-Objekt mit Viewer-Ereignisrückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses ist und der Eigenschaftswert ein JavaScript-Funktionsverweis auf den entsprechenden Rückruf ist. Weitere Informationen zu Viewer-Ereignissen finden Sie im Abschnitt Ereignis-Callbacks . Optional.


## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
