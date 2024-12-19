---
title: init
description: JavaScript-API-Referenz für Basic Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für Basic Zoom Viewer.

`init()`

Startet die Initialisierung des grundlegenden Zoom-Viewers. Zu diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Container-Element noch nicht Teil des Web-Seiten-Layouts ist (z. B. kann es mithilfe `display:none` ihm zugewiesenen Stils ausgeblendet werden), setzt der Viewer seinen Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, an dem die Web-Seite das Container-Element wieder an das Layout zurückgibt. Wenn diese Aktion erfolgt, wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. Nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
