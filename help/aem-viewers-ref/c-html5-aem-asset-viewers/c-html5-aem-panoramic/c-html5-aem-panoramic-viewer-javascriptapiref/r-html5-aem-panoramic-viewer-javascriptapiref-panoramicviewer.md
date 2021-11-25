---
title: PanoramicViewer
description: Erstellen Sie eine neue HTML5-Karussell-Viewer-Instanz.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 13d15bd9483d939de8391d5cfe814c48fed30f22
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructor erstellt eine neue HTML5 Panorama-Viewer-Instanz.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

config {Object} optionales JSON-Konfigurationsobjekt ermöglicht es, alle Viewer-Einstellungen an den Konstruktor zu übergeben und das Aufrufen einzelner Setter-Methoden zu vermeiden. Enthält die folgenden Eigenschaften:
* containerId - {String} ID des DOM-Containers (normalerweise ein DIV), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn init() ausgeführt wird. Erforderlich
* params - {Object} JSON-Objekt mit Viewer-Konfigurationsparametern, bei denen der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder ein SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender settings-Wert ist. Erforderlich
* Handler - {Object} JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert ein JavaScript-Funktionsverweis auf den entsprechenden Rückruf ist. Weitere Informationen zu Viewer-Ereignissen finden Sie im Abschnitt Ereignisrückrufe . Optional


## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
