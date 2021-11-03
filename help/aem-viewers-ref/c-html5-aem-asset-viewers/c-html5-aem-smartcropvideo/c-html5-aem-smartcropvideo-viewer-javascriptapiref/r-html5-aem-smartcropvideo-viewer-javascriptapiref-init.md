---
title: init
description: JavaScript-API-Referenz für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für Smart Crop Video Viewer.

`init()`

Startet die Initialisierung des Smart Crop Video Viewers. Ab diesem Zeitpunkt muss das Container-DOM-Element erstellt werden, damit der Viewer-Code es anhand seiner ID finden kann.

Wenn das Containerelement noch nicht Teil des Webseitenlayouts ist, kann es beispielsweise mit `display:none` Stil zugewiesen - der Viewer setzt den Initialisierungsprozess aus. Dies geschieht bis zu dem Zeitpunkt, zu dem die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion erfolgt, wird der Viewer automatisch neu geladen.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
