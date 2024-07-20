---
title: PanoramicViewer
description: Constructor erstellt eine HTML5 Panorama-Viewer-Instanz.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructor erstellt eine HTML5 Panorama-Viewer-Instanz.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} optionales JSON-Konfigurationsobjekt: Ermöglicht es Ihnen, alle Viewer-Einstellungen an den Konstruktor zu übergeben und einzelne Setter-Methoden zu vermeiden. Sie enthält die folgenden Eigenschaften:

* containerId - {String} Kennung des DOM-Containers (normalerweise ein DIV), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn init() ausgeführt wird. Erforderlich
* params - {Object} JSON-Objekt mit Viewer-Konfigurationsparametern, bei dem der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder einen SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender settings-Wert ist. Erforderlich
* Handler - {Object} JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert eine JavaScript-Funktionsreferenz zum entsprechenden Rückruf ist. Weitere Informationen zu Viewer-Ereignissen finden Sie im Abschnitt Ereignisrückrufe . Optional.


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
