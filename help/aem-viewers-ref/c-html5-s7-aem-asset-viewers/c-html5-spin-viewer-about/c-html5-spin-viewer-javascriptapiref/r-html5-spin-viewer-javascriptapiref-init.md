---
title: init
description: JavaScript-API-Referenz für Rotationsset-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

JavaScript-API-Referenz für Rotationsset-Viewer.

`init()`

Startet die Initialisierung des Rotationsset-Viewers. Durch diese Zeit wird der Container `DOM` -Element erstellt werden, damit der Viewer-Code ihn anhand seiner Kennung finden kann.

Wenn das Containerelement noch nicht Teil des Webseitenlayouts ist, kann es beispielsweise mit `display:none` style - der Viewer setzt seinen Initialisierungsprozess aus. Sie wird ausgesetzt, bis die Webseite das Containerelement wieder in das Layout bringt. Ab diesem Zeitpunkt wird das Laden des Viewers automatisch fortgesetzt.

Rufen Sie diese Methode nur einmal während des Lebenszyklus des Viewers auf. nachfolgende Aufrufe werden ignoriert.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-Instanz.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
